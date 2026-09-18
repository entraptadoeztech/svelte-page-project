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
  height: auto;
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
<script>
  // 1. Define your array of image URLs or paths
  let images = [
    '/IMG_0256.gif',
    '/IMG_0256.gif'
  ];
</script>

<!-- 2. The Marquee Container -->
<div class="marquee-container">
  <!-- We duplicate the track to ensure a seamless, gapless loop -->
  <div class="marquee-track">
    {#each images as img}
      <img src={img} alt="Marquee item" />
    {/each}
  </div>
  
  <div class="marquee-track" aria-hidden="true">
    {#each images as img}
      <img src={img} alt="" />
    {/each}
  </div>
</div>

<style>
  /* Hide scrollbars and clip the edges */
  .marquee-container {
    overflow: hidden;
    display: flex;
    width: 100%;
    user-select: none;
    padding: 10px 0;
  }

  /* The track holds the images and moves left */
  .marquee-track {
    display: flex;
    flex-shrink: 0;
    min-width: 100%;
    gap: 20px; /* Space between images */
    animation: scroll-left 15s linear infinite;
  }

  /* Style your images */
  .marquee-track img {
    height: 100px;
    width: auto;
    object-fit: cover;
    border-radius: 8px;
  }

  /* Pause the animation on hover (optional) */
  .marquee-container:hover .marquee-track {
    animation-play-state: paused;
  }

  /* Keyframe to slide everything left by exactly 100% */
  @keyframes scroll-left {
    from {
      transform: translateX(0%);
    }
    to {
      transform: translateX(-100%);
    }
  }
</style>



