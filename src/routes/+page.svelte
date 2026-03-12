<script>
  import projects from "$lib/projects.json";
  import Project from "$lib/Project.svelte";

  import readings from "$lib/readings.json";
  import Reading from "$lib/Reading.svelte";
  import { onMount } from "svelte";

  let githubData = null; // This will eventually hold our Github stats
  let loading = true; // This will be true *until* the fetch's promise resolves to a value
  let error = null; // If the API call resulted in an error, it will go into this variable

  onMount(async () => {
    try {
      console.log("Page has been mounted!");
      let response = await fetch("https://api.github.com/users/Wendyz1116");
      console.log(response);
      githubData = await response.json();
      console.log(githubData);
    } catch (err) {
      error = err;
    }
    loading = false;
  });
</script>

<h1>Wendy Zhang</h1>
<p>
  Hi! I'm a senior at MIT majoring in Computer Science with a minor in
  Environment and Sustainability
</p>
<img src="images/portrait.jpg" alt="A portrait of Wendy Zhang" width="380" />

<div>
  <h2>My Github Stats</h2>
  {#if loading}
    <p>Loading...</p>
  {:else if error}
    <p>Something went wrong: {error.message}</p>
  {:else}
    <dl class="github-stats">
      <dt>Followers</dt>
      <dd>{githubData.followers}</dd>
      <dt>Following</dt>
      <dd>{githubData.following}</dd>
      <dt>Public Repos</dt>
      <dd>{githubData.public_repos}</dd>
      <dt>Public Gists</dt>
      <dd>{githubData.public_gists}</dd>
    </dl>
  {/if}
</div>

<h2>Latest Projects</h2>
<div class="projects">
  {#each projects.slice(0, 3) as p}
    <Project data={p} />
  {/each}
</div>

<h2>Latest Reading</h2>
<div class="readings">
  {#each readings.slice(0, 3) as r}
    <Reading data={r} />
  {/each}
</div>
