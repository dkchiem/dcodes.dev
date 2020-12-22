<script>
  export let title;
  export let description;
</script>

<style lang="scss">
  .skill {
    padding: 60px 40px;
    border-radius: 20px;
    text-align: center;
    width: 20%;
    min-width: 250px;
    margin: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    filter: drop-shadow(0px 2px 5px rgba(0, 0, 0, 0.2));
    background-color: white;
    #icon {
      height: 150px;
      width: 150px;
      border-radius: 100%;
      background-color: gray;
    }
    * {
      margin: 10px 0;
    }
  }
</style>

<div class="skill" data-scroll data-scroll-type="pop">
  <div id="icon" />
  <h3>{title}</h3>
  <p>{description}</p>
</div>
