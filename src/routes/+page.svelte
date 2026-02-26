<script>
  import projects from "$lib/projects.json";
  import Project from "$lib/Project.svelte";

  import readings from "$lib/readings.json";
  import Reading from "$lib/Reading.svelte";
</script>

<nav>
  <a href="." class="current">Home</a>
  <a href="projects">Projects</a>
  <a href="contact">Contact</a>
  <a href="resume">Resume</a>
  <a href="https://github.com/Wendyz1116" target="_blank">GitHub</a>
</nav>
<h1>Wendy Zhang</h1>
<p>
  Hi! I'm a senior at MIT majoring in Computer Science with a minor in
  Environment and Sustainability
</p>
<img src="images/portrait.jpg" alt="A portrait of Wendy Zhang" width="380" />

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
