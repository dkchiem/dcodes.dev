<script>
  import Header from "@sections/Header.svelte";
  import { onMount } from "svelte";
  import Rellax from "rellax";

  onMount(() => {
    var rellax = new Rellax(".rellax");
  });
</script>

<style lang="scss">
  @keyframes arrowUpDown {
    0% {
      transform: translateX(2px);
    }
    50% {
      transform: translateX(-2px);
    }
    100% {
      transform: translateX(2px);
    }
  }

  section {
    height: 100vh;
    overflow: hidden;
    position: relative;
    #content {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      position: relative;
      height: 70vh;
      #hi {
        margin-bottom: 50px;
      }
      #shapes {
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        grid-gap: calc(10vh / 10);
        .shape {
          height: 10vh;
          width: 10vh;
          &.square {
            border-radius: calc(10vh / 5);
          }
          &.circle {
            border-radius: 100%;
          }
          &.blue {
            background-color: #3e64ff;
            box-shadow: inset calc(10vh / 10) calc(10vh / 10) calc(10vh / 5)
              darken(#3e64ff, 25%);
          }
          &.light-blue {
            background-color: #5edfff;
            box-shadow: inset calc(10vh / 10) calc(10vh / 10) calc(10vh / 5)
              darken(#5edfff, 25%);
          }
          &.gray {
            background-color: #e6e8ea;
            box-shadow: inset calc(10vh / 10) calc(10vh / 10) calc(10vh / 5)
              darken(#e6e8ea, 25%);
          }
        }
      }
    }
    #explore-btn {
      background-color: #3e64ff;
      padding: 10px 30px 10px 20px;
      border-radius: 30px;
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      transform: rotate(-90deg);
      cursor: pointer;
      position: absolute;
      right: 10px;
      bottom: 90px;
      transition: 0.2s;
      span {
        color: white;
        margin-left: 15px;
        font-weight: 700;
      }
      svg {
        transition: 0.2s;
      }
      &:hover {
        background-color: darken(#3e64ff, 25%);
        svg {
          animation: arrowUpDown 0.75s infinite linear;
        }
      }
    }
  }
</style>

<section>
  <Header />
  <div id="content">
    <h1 id="hi" class="rellax" data-rellax-speed="30">Hi.</h1>
    <div id="shapes">
      <!-- row 1 -->
      <div class="shape empty" />
      <div class="shape empty" />
      <div class="shape empty" />
      <div class="shape square blue rellax" data-rellax-speed="14" />
      <div class="shape empty" />
      <!-- row 2 -->
      <div class="shape empty" />
      <div class="shape circle gray rellax" data-rellax-speed="10" />
      <div class="shape square light-blue rellax" data-rellax-speed="6" />
      <div class="shape empty" />
      <div class="shape square light-blue rellax" data-rellax-speed="10" />
      <!-- row 3 -->
      <div class="shape square light-blue rellax" data-rellax-speed="8" />
      <div class="shape square blue rellax" data-rellax-speed="6" />
      <div class="shape circle gray rellax" data-rellax-speed="10" />
      <div class="shape square light-blue rellax" data-rellax-speed="4" />
      <div class="shape circle gray rellax" data-rellax-speed="16" />
    </div>
  </div>
  <a href="#featured-project">
    <div id="explore-btn" data-scroll data-scroll-type="right-fade">
      <svg
        width="20"
        height="20"
        viewBox="0 0 16 20"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <g transform="rotate(90 8 10)">
          <path
            d="M7.29265 19.221C7.68317 19.6115 8.31634 19.6115 8.70686 19.221L15.0708 12.857C15.4613 12.4665 15.4613 11.8334 15.0708 11.4428C14.6803 11.0523 14.0471 11.0523 13.6566 11.4428L7.99976 17.0997L2.3429 11.4428C1.95238 11.0523 1.31921 11.0523 0.928688 11.4428C0.538164 11.8334 0.538164 12.4665 0.928688 12.857L7.29265 19.221ZM6.99976 0.486145L6.99976 18.5139H8.99976L8.99976 0.486145L6.99976 0.486145Z"
            fill="currentcolor" />
        </g></svg>
      <span>Explore</span>
    </div>
  </a>
</section>
