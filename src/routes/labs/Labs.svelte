<script lang="ts">
  import { Accordion, Tabs } from "@skeletonlabs/skeleton-svelte";

  let group = $state("lab1");
  let value = $state([""]);
</script>

<div
  class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y overflow-hidden"
>
  <Tabs value={group} onValueChange={(e) => (group = e.value)} fluid>
    {#snippet list()}
      <Tabs.Control value="lab1">Lab 1</Tabs.Control>
       <Tabs.Control value="lab2">Lab 2</Tabs.Control>
      <Tabs.Control value="lab34">Labs 3 & 4</Tabs.Control>
    {/snippet}
    {#snippet content()}
      <Tabs.Panel value="lab1">
        <Accordion {value} onValueChange={(e) => (value = e.value)} collapsible>
          <Accordion.Item value="outline">
            <!-- Control -->
            {#snippet control()}Team Outline{/snippet}
            <!-- Panel -->
            {#snippet panel()}
              <article class="space-y-2 p-4">
                <iframe
                  src="https://docs.google.com/document/d/e/2PACX-1vQOmUq5oIOYB-PJYY6zwtcVI1shSL-poTObS2IZOUonHDsVfZXYODo27FMYxChgeraYgyCY_BtbYsWa/pub?embedded=true"
                  title="Lab 1 Outline"
                  class="container h-[calc(100vh-25rem)]"
                  allowfullscreen
                ></iframe>
              </article>
            {/snippet}
          </Accordion.Item>
          <!-- COPY THIS FOR EACH MEMBER. (Change value to be unique and use names accordingly)-->
          <Accordion.Item value="gabriel_lugo">
            <!-- Control -->
            {#snippet control()}Gabriel Lugo{/snippet}
            <!-- Panel -->
            {#snippet panel()}
              <article class="space-y-2 p-4">
                <embed
                  src="/labs/lab1_roguelike_algebra_lugo_version_1.pdf"
                  type="application/pdf"
                  class="h-[calc(100vh-25rem)] w-full"
                />
              </article>
            {/snippet}
          </Accordion.Item>

          <Accordion.Item value="Brennen_Gabriel">
            <!-- Control -->
            {#snippet control()}Brennen Gabriel{/snippet}
            <!-- Panel -->
            {#snippet panel()}
              <article class="space-y-2 p-4">
                <embed
                  src="/labs/lab1_roguelike_algebra_Brennen_version_1.pdf"
                  type="application/pdf"
                  class="h-[calc(100vh-25rem)] w-full"
                />
              </article>
            {/snippet}
          </Accordion.Item>

          <Accordion.Item value="jillian_cequeria">
            <!-- Control -->
            {#snippet control()}Jillian Cequeria{/snippet}
            <!-- Panel -->
            {#snippet panel()}
              <article class="space-y-2 p-4">
                <embed
                  src="/labs/lab1_roguelike_algebra_cequeria_version_1.pdf"
                  type="application/pdf"
                  class="h-[calc(100vh-25rem)] w-full"
                />
              </article>
            {/snippet}
          </Accordion.Item>

          <Accordion.Item value="jacob_thompson">
            <!-- Control -->
            {#snippet control()}Jacob Thompson{/snippet}
            <!-- Panel -->
            {#snippet panel()}
              <article class="space-y-2 p-4">
                <embed
                  src="/labs/lab1_roguelike_algebra_jacob_version_1.pdf"
                  type="application/pdf"
                  class="h-[calc(100vh-25rem)] w-full"
                />
              </article>
            {/snippet}
          </Accordion.Item>

          <!-- END REGION TO COPY -->
        </Accordion>
      </Tabs.Panel>

      <!--Lab 2 Panel-->
      <Tabs.Panel value="lab2">
        <Accordion {value} onValueChange={(e) => (value = e.value)} collapsible>
          <!-- COPY THIS FOR EACH MEMBER. (Change value to be unique and use names accordingly)-->

          <Accordion.Item value="Brennen_Gabriel">
            <!-- Control -->
            {#snippet control()}Brennen Gabriel{/snippet}
            <!-- Panel -->
            {#snippet panel()}
              <article class="space-y-2 p-4">
                <embed
                  src="labs/Lab2_rogulelike_algebra_Brennen_version_2.pdf"
                  type="application/pdf"
                  class="h-[calc(100vh-25rem)] w-full"
                />
              </article>
            {/snippet}
          </Accordion.Item>

          <!-- END REGION TO COPY -->

          <Accordion.Item value="jillian_cequeria">
            <!-- Control -->
            {#snippet control()}Jillian Cequeria{/snippet}
            <!-- Panel -->
            {#snippet panel()}
              <article class="space-y-2 p-4">
                <embed
                  src="labs/lab2_roguelike_algebra_cequeria_version_2.pdf"
                  type="application/pdf"
                  class="h-[calc(100vh-25rem)] w-full"
                />
              </article>
            {/snippet}
          </Accordion.Item>

        </Accordion>
      </Tabs.Panel>

      <Tabs.Panel value="lab34">
        <article class="space-y-2 p-4">
          Link to User Manual:
          <a
            href="https://github.com/gold-team-odu/gold-team-odu.github.io/wiki"
            class="underline"
            >https://github.com/gold-team-odu/gold-team-odu.github.io/wiki</a
          >
        </article>
      </Tabs.Panel>
    {/snippet}
  </Tabs>
</div>
