<svelte:head>
  <title>Contact me</title>
</svelte:head>
<nav>
  <a href="./">Home</a>
  <a href="../projects">Projects</a>
  <a href="./" class="current">Contact</a>
  <a href="../resume">Resume</a>
  <a href="https://github.com/Wendyz1116" target="_blank">GitHub</a>
</nav>
<h1>Contact</h1>
<form action="mailto:wendyz@mit.edu" method="GET">
  <label
    >Email
    <input name="email" type="email" />
  </label>
  <label
    >Subject
    <input name="subject" />
  </label>
  <label
    >Message
    <textarea name="body"></textarea>
  </label>
  <button>Submit</button>
</form>
