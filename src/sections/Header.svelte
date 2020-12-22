<script>
  import Navbar from "@components/Navbar.svelte";
</script>

<style lang="scss">
  header {
    height: 150px;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    position: relative;
    #brand {
      display: flex;
      align-items: center;
      justify-content: center;
      position: absolute;
      left: 10%;
      #logo {
        font-size: 3rem;
        font-family: "Monoton", cursive;
        margin-right: 15px;
      }
    }
  }
</style>

<header>
  <div id="brand">
    <span id="logo">D</span>
    <h3>Vu Dang Khoa Chiem</h3>
  </div>
  <Navbar />
</header>
