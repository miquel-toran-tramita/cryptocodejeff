<script lang="ts">
  import { onMount } from 'svelte'

  let jeffPosition = 0

  onMount(() => {
    document.addEventListener('scroll', () => {
      console.log(window.scrollY)

      const newPosition = Math.floor(window.scrollY / 100)

      if (newPosition < 6) jeffPosition = newPosition
    })
  })
</script>

<style lang="scss">
  .hero {
    display: flex;
    gap: 100px;
    padding: 50px 0;

    img {
      position: sticky;
      top: 50px;
    }

    .block {
      padding-bottom: 50px;
    }
    p,
    h1 {
      font-size: 40px;
      font-weight: bold;
    }

    span {
      background: linear-gradient(to bottom right, #00bbb8 0%, #69bb2d 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
  }
</style>

<div class="hero g-wrapper">
  <img src="/assets/jeff/jeff{jeffPosition}.png" alt="" width="128" height="220" />

  <div class="text">
    <div class="block">
      <p style="font-size: 80px" reveal>
        Hi! I'm <span>Jeff</span>,
      </p>

      <p reveal="0.6">The piece that your project needs,</p>
    </div>

    <div class="block">
      <p reveal="0.7">Behind a succesful meme coin there's a consolidated community that lives off</p>
      <p reveal="0.8"><span> trust and resilience</span>.</p>
    </div>

    <div class="block">
      <p reveal="0.9">More essential than that,</p>
      <p reveal="1">there's a dev, a leader,</p>
      <p reveal="1.1">cooking the details <span>with love</span>.</p>
    </div>

    <div class="block">
      <h1 reveal="1.2">A showy website <span>can make the difference</span>.</h1>
      <p reveal="1.3">Jeff can help with that!</p>
    </div>
  </div>
</div>
