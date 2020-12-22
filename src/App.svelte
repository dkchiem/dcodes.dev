<script>
  import Hello from "@sections/Hello.svelte";
  import FeaturedProject from "@sections/FeaturedProject.svelte";
  import Skills from "@sections/Skills.svelte";
  import Work from "@sections/Work.svelte";
  import Footer from "@sections/Footer.svelte";

  import { onMount } from "svelte";
  import ScrollOut from "scroll-out";

  onMount(() => {
    ScrollOut({
      threshold: 0.5,
      once: true,
    });
  });
</script>

<style lang="scss">
</style>

<svelte:head>
  <title>dcodes.dev</title>
</svelte:head>

<Hello />
<FeaturedProject />
<Skills />
<hr />
<Work />
<Footer />
