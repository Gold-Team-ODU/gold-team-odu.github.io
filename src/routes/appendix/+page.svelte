<script lang="ts">
  import { Accordion } from "@skeletonlabs/skeleton-svelte";
  import PageTitle from "../PageTitle.svelte";
  import References from "./References.svelte";
  import Glossary from "./Glossary.svelte";

  let value = $state([""]);
</script>

<svelte:head>
  <PageTitle page={"Appendix"} />
</svelte:head>

<div class="mx-auto">
  <div class="container grid grid-cols-[auto_1fr] p-2">
    <header
      class="h2 px-5 [writing-mode:vertical-lr] rotate-180 place-self-start"
    >
      Extra Resources
    </header>
    <article class="text-justify pl-5 text-base xl:text-lg">
      <div
        class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
      >
        <Accordion {value} onValueChange={(e) => (value = e.value)} collapsible>
          <Accordion.Item value="glossary">
            <!-- Control -->
            {#snippet lead()}
              <span class="material-symbols-rounded"> book_6 </span>
            {/snippet}
            {#snippet control()}Glossary{/snippet}
            <!-- Panel -->
            {#snippet panel()}<Glossary />{/snippet}
          </Accordion.Item>
          <Accordion.Item value="references">
            <!-- Control -->
            {#snippet lead()}
              <span class="material-symbols-rounded"> search_insights </span>
            {/snippet}
            {#snippet control()}References{/snippet}
            <!-- Panel -->
            {#snippet panel()}<References />{/snippet}
          </Accordion.Item>

          <!-- <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
          {#snippet list()}
            <Tabs.Control value="glossary">Glossary</Tabs.Control>
            <Tabs.Control value="references">References</Tabs.Control>
          {/snippet}
          {#snippet content()}
            <Tabs.Panel value="references">
              <article class="space-y-2 p-4">
                <References />
              </article>
            </Tabs.Panel>
            <Tabs.Panel value="glossary">
              <article class="space-y-2 p-4">
                <Glossary />
              </article>
            </Tabs.Panel>
          {/snippet}
        </Tabs> -->
        </Accordion>
      </div>
    </article>
  </div>
</div>

<style>
</style>
