<script lang="ts">
  import { onMount } from "svelte";

  import "../app.css";

  import Tabs from "./Tabs.svelte";

  import { Avatar } from "@skeletonlabs/skeleton-svelte";

  let scrollY = $state(0);
  let isAtTop = $derived(scrollY <= 10); // Small threshold to account for slight movements

  onMount(() => {
    const handleScroll = () => {
      scrollY = window.scrollY;
    };

    window.addEventListener("scroll", handleScroll);

    return () => {
      window.removeEventListener("scroll", handleScroll);
    };
  });
</script>

<header
  class="sticky top-0 z-50 w-full {isAtTop
    ? 'rounded-3xl'
    : 'rounded-b-3xl rounded-t-none'}"
>
  <div class="relative">
    <div
      class="absolute -inset-0 preset-glass-surface {isAtTop
        ? 'rounded-3xl'
        : 'rounded-b-3xl rounded-t-none'}"
    ></div>
    <div class="relative grid grid-cols-[1fr_auto] gap-2 p-5">
      <div class="grid grid-cols-[auto_auto_1fr] items-center gap-2">
        <!-- Thanks stack overflow https://stackoverflow.com/a/74753353/17004103-->
        <a
          href="/"
          class="font-[Markazi_Text] text-3xl md:text-4xl font-extrabold md:visible text-surface-950-50 drop-shadow-[0_0px_0.5px_rgba(0,0,0,0)] drop-shadow-surface-950"
        >
          <p>Rogue-like Algebra</p>
        </a>

        <span
          class="vr max-md:invisible max-md:w-0 border-l-2 border-surface-700"
        ></span>

        <p
          class="max-md:invisible max-md:w-0 text-xs text-surface-700-300 drop-shadow-[0_0px_0.5px_rgba(0,0,0,0)] drop-shadow-surface-950"
        >
          by the <span
            class="font-semibold text-shadow-[0_0_20px_rgba(0,0,0,0)] text-shadow-amber-400/50"
            >Gold</span
          > Team
        </p>
      </div>

      <div class="grid grid-cols-2 gap-2">
        <a href="https://odu.edu" class="drop-shadow-lg/30">
          <Avatar src="/img/odu.jpg" name="ODU" />
        </a>
        <a href="https://cs.odu.edu" class="drop-shadow-lg/30">
          <Avatar src="/img/odu_cs.jpg" name="CS ODU" />
        </a>
      </div>
    </div>
    <Tabs />
  </div>
</header>

<style>
  :global(#smui-app),
  :global(body),
  :global(html) {
    display: block !important;
    height: auto !important;
    width: auto !important;
    position: static !important;
  }

  .preset-glass-surface {
    background: color-mix(
      in oklab,
      var(--color-surface-50-950) 40%,
      transparent
    );
    box-shadow: 0 0px 30px
      color-mix(in oklab, var(--color-surface-50-950) 50%, transparent) inset;
    backdrop-filter: blur(16px);
  }
</style>
