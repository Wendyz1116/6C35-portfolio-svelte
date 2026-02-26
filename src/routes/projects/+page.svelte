<script>
  import projects from "$lib/projects.json";
  import Project from "$lib/Project.svelte";
</script>

<svelte:head>
  <title>Projects</title>
</svelte:head>

<nav>
  <a href=".">Home</a>
  <a href="projects" class="current">Projects</a>
  <a href="contact">Contact</a>
  <a href="resume">Resume</a>
  <a href="https://github.com/Wendyz1116" target="_blank">GitHub</a>
</nav>
<h1>Projects</h1>

<div class="projects">
  {#each projects as p}
    <Project data={p} />
  {/each}
  <!-- <article>
    <h2>Assignment 2: Exploratory Visual Analysis</h2>
    <img src="https://vis-society.github.io/labs/2/images/empty.svg" alt="" />
    <a href="A2_report.html">View Assignment 2 Report</a>
  </article> -->
</div>
