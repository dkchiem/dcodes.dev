<script>
  import Project from "@components/Project.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    const evenProjects = document.querySelectorAll(
      "#work .project:nth-child(even)"
    );
    const oddProjects = document.querySelectorAll(
      "#work .project:nth-child(odd)"
    );
    evenProjects.forEach((project) => {
      project.setAttribute("data-scroll-type", "left-fade");
    });
    oddProjects.forEach((project) => {
      project.setAttribute("data-scroll-type", "right-fade");
    });
  });
</script>

<style lang="scss">
  section {
    padding: 100px 10%;
    overflow: hidden;
  }
</style>

<section id="work">
  <Project
    topTitle="Featured Project"
    title="Vortex Design System"
    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin turpis
  urna, iaculis nec leo a, tincidunt dignissim neque. In eu vehicula lectus,
  et elementum orci. Suspendisse porta, odio sit amet interdum luctus, nibh
  orci aliquam leo, at placerat lacus nibh sit amet odio. Donec lectus ante,
  posuere porta nisi at, faucibus venenatis est. Sed quis consectetur
  lectus. Integer fringilla interdum nibh, id feugiat tellus euismod ac.
  Quisque ut ornare ipsum. In vulputate et velit vel condimentum." />
  <Project
    topTitle="Featured Project"
    title="Vortex Design System"
    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin turpis
  urna, iaculis nec leo a, tincidunt dignissim neque. In eu vehicula lectus,
  et elementum orci. Suspendisse porta, odio sit amet interdum luctus, nibh
  orci aliquam leo, at placerat lacus nibh sit amet odio. Donec lectus ante,
  posuere porta nisi at, faucibus venenatis est. Sed quis consectetur
  lectus. Integer fringilla interdum nibh, id feugiat tellus euismod ac.
  Quisque ut ornare ipsum. In vulputate et velit vel condimentum." />
  <Project
    topTitle="Featured Project"
    title="Vortex Design System"
    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin turpis
  urna, iaculis nec leo a, tincidunt dignissim neque. In eu vehicula lectus,
  et elementum orci. Suspendisse porta, odio sit amet interdum luctus, nibh
  orci aliquam leo, at placerat lacus nibh sit amet odio. Donec lectus ante,
  posuere porta nisi at, faucibus venenatis est. Sed quis consectetur
  lectus. Integer fringilla interdum nibh, id feugiat tellus euismod ac.
  Quisque ut ornare ipsum. In vulputate et velit vel condimentum." />
  <Project
    topTitle="Featured Project"
    title="Vortex Design System"
    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin turpis
  urna, iaculis nec leo a, tincidunt dignissim neque. In eu vehicula lectus,
  et elementum orci. Suspendisse porta, odio sit amet interdum luctus, nibh
  orci aliquam leo, at placerat lacus nibh sit amet odio. Donec lectus ante,
  posuere porta nisi at, faucibus venenatis est. Sed quis consectetur
  lectus. Integer fringilla interdum nibh, id feugiat tellus euismod ac.
  Quisque ut ornare ipsum. In vulputate et velit vel condimentum." />
  <Project
    topTitle="Featured Project"
    title="Vortex Design System"
    description="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin turpis
  urna, iaculis nec leo a, tincidunt dignissim neque. In eu vehicula lectus,
  et elementum orci. Suspendisse porta, odio sit amet interdum luctus, nibh
  orci aliquam leo, at placerat lacus nibh sit amet odio. Donec lectus ante,
  posuere porta nisi at, faucibus venenatis est. Sed quis consectetur
  lectus. Integer fringilla interdum nibh, id feugiat tellus euismod ac.
  Quisque ut ornare ipsum. In vulputate et velit vel condimentum." />
</section>
