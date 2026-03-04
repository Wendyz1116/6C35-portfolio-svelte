<script>
  import { base } from "$app/paths";
  // store is special Svelte object that automatically updates whenever its value changes
  //   with $
  import { page } from "$app/stores";
  import "../style.css";

  let pages = [
    { url: "/", title: "Home" },
    { url: "/projects", title: "Projects" },
    { url: "/contact", title: "Contact" },
    { url: "/resume", title: "Resume" },
    { url: "https://github.com/Wendyz1116", title: "GitHub" },
  ];

  let colorScheme = "light dark";

  let localStorage = globalThis.localStorage ?? {};

  if (localStorage.colorScheme) {
    // if localStorage has a colorScheme property
    colorScheme = localStorage.colorScheme; // override the default colorScheme
  }

  let root = globalThis.document?.documentElement;
  // $: prefix re-run this every time any of its dependencies change, reactive statement,
  $: root?.style.setProperty("color-scheme", colorScheme);

  $: localStorage.colorScheme = colorScheme;
</script>

<label class="color-scheme-switch">
  Theme:
  <select bind:value={colorScheme}>
    <option value="light dark">Automatic</option>
    <option value="light">Light</option>
    <option value="dark">Dark</option>
  </select>
</label>

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

<style>
  nav {
    --border-color: oklch(50% 10% 200 / 40%);
    display: flex;
    margin-bottom: 0.5em;
    border-bottom-width: 1px;
    border-bottom-style: solid;
    border-bottom-color: var(--border-color);
  }

  nav a {
    flex: 1;
    text-decoration: none;
    color: inherit;
    text-align: center;
    padding: 0.5em;
  }

  a.current {
    border-bottom-width: 0.4em;
    border-bottom-style: solid;
    padding-bottom: -0.2em;
    border-bottom-color: var(--border-color);
  }

  a:hover {
    border-bottom-width: 0.4em;
    border-bottom-style: solid;
    padding-bottom: -0.2em;
    border-color: var(--color-accent);
    background-color: oklch(from var(--color-accent) l c h / 0.3);
  }

  .color-scheme-switch {
    position: absolute;
    top: 1rem;
    right: 1rem;
    display: inline-flex;
    gap: 5px;
    font-size: 80%;
  }
</style>
