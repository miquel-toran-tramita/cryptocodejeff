<style lang="scss">
  .value {
    position: relative;
    height: 50vh;
    padding: 50px 0;

    .candles {
      position: absolute;
      z-index: -1;
      filter: saturate(20%) blur(7px);
      opacity: 0.2;
      left: 0;
      top: -50vh;
    }

    p {
      padding: 50px 0;
      font-size: 30px;
    }
  }
</style>

<div class="value">
  <img class="candles" src="/assets/candles.png" width="100%" alt="" />
  <div class="g-wrapper">
    <h2>Jeff's current value</h2>

    <p>
      Time is limited, but Jeff is very flexible, let's get in touch and make an analysis of your project for free and set a fair price for
      both.
    </p>
    <div class="cards"></div>
  </div>
</div>
