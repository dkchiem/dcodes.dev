<script>
  let navOpen = false;

  function openSidenav() {
    navOpen = true;
  }

  function closeSidenav() {
    navOpen = false;
  }
</script>

<style lang="scss">
  // Small screens
  @media only screen and (max-width: 920px) {
    svg {
      display: block;
    }
    nav {
      position: fixed;
      height: 100vh;
      width: 0;
      top: 0;
      right: 0;
      background-color: white;
      z-index: 1000;
      ul {
        position: absolute;
        left: 60px;
        flex-direction: column;
        margin-top: 80px;
      }
      #x-hamburger-menu {
        display: none;
        position: absolute;
        top: 30px;
        left: 30px;
        cursor: pointer;
        &.on {
          display: block;
        }
      }
      &.open {
        width: 50%;
      }
      @media only screen and (max-width: 600px) {
        &.open {
          width: 100%;
        }
      }
    }
  }

  // Large screens
  @media only screen and (min-width: 920px) {
    svg {
      display: none;
    }
    nav {
      align-items: center;
      ul {
        position: absolute;
        right: 10%;
      }
      #x-hamburger-menu {
        display: none;
      }
    }
    #overlay {
      display: none;
    }
  }

  #hamburger-menu {
    position: absolute;
    right: 10%;
    cursor: pointer;
  }

  nav {
    display: flex;
    justify-content: center;
    transition: right 0.3s;
    overflow: hidden;
    transition: width 0.5s;
    ul {
      display: flex;
      li {
        list-style: none;
        padding: 20px 30px;
        a {
          text-decoration: none;
          white-space: nowrap;
        }
      }
    }
  }

  #overlay {
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100vw;
    background-color: rgba(0, 0, 0, 0.5);
    opacity: 0.5;
    z-index: 500;
    transition: visibility 0.3s linear, opacity 0.3s linear;
    visibility: hidden;
    opacity: 0;
    &.on {
      opacity: 1;
      visibility: visible;
    }
  }
</style>

<svg
  width="35"
  height="35"
  viewBox="0 0 24 24"
  id="hamburger-menu"
  fill="none"
  on:click={openSidenav}>
  <path
    d="M9 5H22M2 12H22M2 19H22"
    stroke="black"
    stroke-width="2"
    stroke-linecap="round" />
</svg>

<nav class:open={navOpen}>
  <svg
    width="35"
    height="35"
    viewBox="0 0 24 24"
    id="x-hamburger-menu"
    fill="none"
    class:on={navOpen}
    on:click={closeSidenav}>
    <path
      d="M5.41421 5.00001L19.5563 19.1421M5 19.1421L19.1421 5"
      stroke="black"
      stroke-width="2"
      stroke-linecap="round" />
  </svg>

  <ul>
    <li>
      <a class="drawline" on:click={closeSidenav} href="#skills">My Skills</a>
    </li>
    <li>
      <a class="drawline" on:click={closeSidenav} href="#work">My Work</a>
    </li>
    <li><a class="drawline" on:click={closeSidenav} href="">Contact Me</a></li>
  </ul>
</nav>

<div id="overlay" class:on={navOpen} on:click={closeSidenav} />
