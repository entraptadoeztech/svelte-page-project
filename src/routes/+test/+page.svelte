<svelte:head>
  <title>Felix</title>
</svelte:head>

<h1>Testing</h1>

<p>
  This website loads faster than a typical HTML site. Wow.
</p>

<img
  src="/IMG_1332.jpeg"
  alt="Felix"
  loading="lazy"
  decoding="async"
/>
<p>It's felix!</p>
<nav class="links" aria-label="Main navigation">
  <a href="/">Home</a>
</nav>

<style>
  h1 {
    margin-bottom: 1rem;
  }
body{
background-color:#2c14ff;
}

  p {
    margin-bottom: 1rem;
    line-height: 1.5;
    color:plum
  }

  .links {
    display: flex;
    gap: 1rem;
    margin-top: 1rem;
  }

  .links a {
    color: #2563eb;
    text-decoration: none;
  }

  .links a:hover {
    text-decoration: underline;
  }

  img {
    display: block;
    max-width: 100%;
    height: auto;
    border-radius: 8px;
    margin: 1rem 0;
  }
</style>
