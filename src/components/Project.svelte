<script>
  export let topTitle;
  export let title;
  export let description;
</script>

<style lang="scss">
  .project {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 100px;
    #image {
      display: flex;
      align-items: center;
      justify-content: center;
      img {
        height: 300px;
      }
    }
    > * {
      flex: 1;
    }
    &:nth-child(even) {
      flex-direction: row-reverse;
    }
  }
</style>

<div class="project" data-scroll>
  <div>
    <h4>{topTitle}</h4>
    <h2>{title}</h2>
    <p>{description}</p>
  </div>
  <div id="image"><img src="../assets/vortex-logo.png" alt="" /></div>
</div>
