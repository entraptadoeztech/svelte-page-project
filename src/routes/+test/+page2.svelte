<svelte:head>
  <title>Felix</title>
</svelte:head>

<h1>Fan art!</h1>
<nav class="links" aria-label="Main navigation">
  <a href="/">Home</a>
</nav>
<img
  src="/IMG_0309.gif"
  alt="Felix"
  loading="lazy"
  decoding="async"
/>
<img
  src="/IMG_1334.jpeg"
  alt="Felix"
  loading="lazy"
  decoding="async"
/>
<br>
<img
  src="/IMG_1336.jpeg"
  alt="Felix"
  loading="lazy"
  decoding="async"
/>
<style>
  h1 {
    margin-bottom: 1rem;
  }
html {
background-color:#2c14ff;
}

  p {
    margin-bottom: 1rem;
    line-height: 1.5;
    color:plum;
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
<marquee behavior="scroll" direction="left" scrollamount="6">
  <img src="/IMG_0256.gif" alt="Image 1" style="height: 100px; margin-right: 20px;">
  <img src="/IMG_0258.gif" alt="Image 2" style="height: 100px; margin-right: 20px;">
</marquee>


