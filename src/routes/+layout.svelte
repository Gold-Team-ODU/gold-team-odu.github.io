<script lang="ts">
  import "../app.css";

  import { onMount } from "svelte";
  import { fade } from "svelte/transition";

  import { ProgressRing } from "@skeletonlabs/skeleton-svelte";

  import Header from "./Header.svelte";
  import Footer from "./Footer.svelte";

  let ready = $state(false);
  onMount(() => {
    ready = true;
  });

  let { children } = $props();
</script>

<div class="container mx-auto h-screen w-full flex justify-center">
  {#if ready}
    <!-- Fade in content pane -->
    <div
      class="w-full min-h-screen max-w-xl md:max-w-4xl 2xl:max-w-7xl"
      in:fade={{ duration: 500, delay: 100 }}
    >
      <!-- Primary content -->
      <div class="relative">
        <!-- Shadow -->
        <div
          class="absolute -inset-0.5 bg-surface-500 opacity-75 blur-[0px] rounded-3xl"
        ></div>
        <!-- Panel -->
        <div class="min-h-screen relative bg-surface-100-900 rounded-3xl">
          <div class="min-h-screen grid grid-rows-[auto_1fr_auto] gap-5">
            <Header />

            <main class="px-5 h-full">
              {@render children?.()}
            </main>

            <Footer />
          </div>
        </div>
      </div>
    </div>
  {:else}
    <div class="container flex mx-auto w-screen min-h-screen justify-center">
      <div class="container w-fit min-h-screen place-content-center">
        <ProgressRing
          value={null}
          size="size-20"
          meterStroke="stroke-tertiary-600-400"
          trackStroke="stroke-tertiary-50-950"
        />
      </div>
    </div>
  {/if}
</div>

<style>
  :global(#smui-app),
  :global(body),
  :global(html) {
    display: block !important;
    height: auto !important;
    width: auto !important;
    position: static !important;
  }
</style>
