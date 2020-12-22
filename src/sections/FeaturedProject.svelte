<style lang="scss">
  // Small screens
  @media only screen and (max-width: 820px) {
    section {
      flex-direction: column;
    }
  }

  // // Large screens
  // @media only screen and (min-width: 920px) {
  // }

  section {
    background-color: #ecfcff;
    padding: 50px 10%;
    display: flex;
    align-items: center;
    justify-content: center;
    #image {
      display: flex;
      align-items: center;
      justify-content: center;
      img {
        height: 300px;
        width: 300px;
      }
    }
    > * {
      flex: 1;
    }
  }
</style>

<section id="featured-project">
  <div>
    <h4>Featured Project</h4>
    <h2>Vortex Design System</h2>
    <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin turpis
      urna, iaculis nec leo a, tincidunt dignissim neque. In eu vehicula lectus,
      et elementum orci. Suspendisse porta, odio sit amet interdum luctus, nibh
      orci aliquam leo, at placerat lacus nibh sit amet odio. Donec lectus ante,
      posuere porta nisi at, faucibus venenatis est. Sed quis consectetur
      lectus. Integer fringilla interdum nibh, id feugiat tellus euismod ac.
      Quisque ut ornare ipsum. In vulputate et velit vel condimentum.
    </p>
  </div>
  <div id="image"><img src="../assets/vortex-logo.png" alt="" /></div>
</section>
