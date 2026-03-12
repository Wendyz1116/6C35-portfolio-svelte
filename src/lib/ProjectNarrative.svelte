<script>
  import Scrolly from "svelte-scrolly";
  import { base } from "$app/paths";
  import projects from "$lib/projects.json";
  let sorted_projects = projects.sort((a, b) => a.year - b.year);

  let scrollyProgress = 0;

  let progressPerProject = 100 / sorted_projects.length;
  $: activeProjectIdx = Math.min(
    sorted_projects.length - 1,
    Math.floor(scrollyProgress / progressPerProject),
  );
</script>

<div class="scrolly-wrapper">
  <Scrolly bind:progress={scrollyProgress}>
    {#each sorted_projects as project}
      <section class="step">
        <div class="step-content">
          <h3>{project.title}</h3>
          <p>{project.story}</p>
        </div>
      </section>
    {/each}

    <svelte:fragment slot="viz">
      <div class="project-detail">
        <h3>{sorted_projects[activeProjectIdx].year}</h3>
        <img
          src="{base}{sorted_projects[activeProjectIdx].image}"
          alt={sorted_projects[activeProjectIdx].title}
        />
      </div>
    </svelte:fragment>
  </Scrolly>
</div>

<style>
  .scrolly-wrapper {
    width: 90vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
  }

  .step {
    min-height: 80vh;
    padding: 0.5rem 0.5rem 0.5rem 0;
  }

  .step-content {
    border-left: solid var(--color-accent);
    padding: 1.5rem 1rem;
  }

  .project-detail {
    padding: 1rem;
    width: 100%;
  }

  .project-detail img {
    width: 100%;
  }
</style>
