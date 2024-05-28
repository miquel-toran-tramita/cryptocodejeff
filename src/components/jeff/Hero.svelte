<script lang="ts">
  import { onMount } from 'svelte'

  let jeffPosition = 0

  onMount(() => {
    document.addEventListener('scroll', () => {
      console.log(window.scrollY)

      const newPosition = Math.floor(window.scrollY / 100)

      if (newPosition < 7) jeffPosition = newPosition
    })
  })
</script>

<style lang="scss">
  .hero {
    display: flex;
    gap: 150px;
    padding-top: 100px;

    img {
      position: sticky;
      top: 50px;
      margin-left: 20px;
    }

    .text {
      padding-bottom: 200px;
    }

    .block {
      padding-bottom: 50px;
    }
    p,
    h1 {
      font-size: 40px;
      font-weight: bold;
    }
  }
</style>

<div class="hero g-wrapper">
  <img src="/assets/jeff/jeff{jeffPosition}.png" alt="" width="128" height="220" />

  <div class="text">
    <div class="block">
      <p style="font-size: 80px" reveal>
        Hi! I'm <span class="g-text">Jeff</span>,
      </p>

      <p reveal="0.6">The piece that your project needs,</p>
    </div>

    <div class="block">
      <p reveal="0.7">Behind a succesful meme coin there's a consolidated community that lives off</p>
      <p reveal="0.8"><span class="g-text"> trust and resilience</span>.</p>
    </div>

    <div class="block">
      <p reveal="0.9">More essential than that,</p>
      <p reveal="1">there's a dev, a leader,</p>
      <p reveal="1.1">cooking the details <span class="g-text">with love</span>.</p>
    </div>

    <div class="block">
      <h1 reveal="1.2">A showy website <span class="g-text">can make the difference</span>.</h1>
      <br />
      <p reveal="1.3">Jeff can help with that!</p>
    </div>
  </div>
</div>
