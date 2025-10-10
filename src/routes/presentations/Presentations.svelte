<script lang="ts">
  import { Tabs } from "@skeletonlabs/skeleton-svelte";

  let group = $state("societal_problem");
</script>

<div
  class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
>
  <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
    {#snippet list()}
      <Tabs.Control value="societal_problem">Societal Problem</Tabs.Control>
      <Tabs.Control value="feasibility">Feasibility</Tabs.Control>
      <Tabs.Control value="design">Design</Tabs.Control>
    {/snippet}
    {#snippet content()}
      <Tabs.Panel value="societal_problem">
        <article class="space-y-2 p-4">
          <embed
            src="/presentations/societal_problem.pdf"
            type="application/pdf"
            class="h-[calc(100vh-25rem)] w-full"
          />
        </article>
      </Tabs.Panel>
      <Tabs.Panel value="feasibility">
        <article class="space-y-2 p-4">
          <embed
            src="/presentations/feasibility.pdf"
            type="application/pdf"
            class="h-[calc(100vh-25rem)] w-full"
          />
        </article>
      </Tabs.Panel>
      <Tabs.Panel value="design">
        <article class="space-y-2 p-4">
          <embed
            src="/presentations/formal_design.pdf"
            type="application/pdf"
            class="h-[calc(100vh-25rem)] w-full"
          />
        </article>
      </Tabs.Panel>
    {/snippet}
  </Tabs>
</div>
