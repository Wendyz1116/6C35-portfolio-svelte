<script>
  import { base } from "$app/paths";
  // store is special Svelte object that automatically updates whenever its value changes
  //   with $
  import { page } from "$app/stores";

  let pages = [
    { url: "/", title: "Home" },
    { url: "/projects", title: "Projects" },
    { url: "/contact", title: "Contact" },
    { url: "/resume", title: "Resume" },
    { url: "https://github.com/Wendyz1116", title: "GitHub" },
  ];
</script>

<nav>
  {#each pages as p}
    <a
      href={base + p.url}
      class:current={p.url === "/" // is this link the home page?
        ? $page.url.pathname === base + "/" // if yes - set current = true if the path name matches. Else, set current = true if the path name starts correctly
        : $page.url.pathname.startsWith(base + p.url)}
      target={p.url.startsWith("http") ? "_blank" : null}>{p.title}</a
    >
  {/each}
</nav>
<slot />
