<script lang="ts">
  import PageTitle from "../PageTitle.svelte";

  let group = $state("problem");
</script>

<svelte:head>
  <PageTitle page={"Team"} />
</svelte:head>

<div class="mx-auto">
  <div class="container grid grid-cols-[auto_1fr] p-2">
    <header
      class="h2 px-5 [writing-mode:vertical-lr] rotate-180 place-self-start"
    >
      Meet the Team
    </header>
    <article class="text-justify pl-5 text-base xl:text-lg">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-2">
        <div
          class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y divide- overflow-hidden"
        >
          <img
            src="/img/mem/brennen_gabriel.jpg"
            alt="brennen_gabriel"
            class="aspect-[12/9] w-full object-cover object-[0_100%]"
          />
          <article class="space-y-4 p-4">
            <div class="h2">Brennen Gabriel</div>
            <p class="opacity-60">
              Brennen Gabriel earned dual degrees in Marketing and Economics
              from the University of Kentucky. He is now a senior at Old
              Dominion University, pursuing a degree in Computer Science.
            </p>
          </article>
        </div>
        <div
          class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y divide- overflow-hidden"
        >
          <img
            src="/img/mem/gabriel_lugo.jpg"
            alt="gabriel_lugo"
            class="aspect-[12/9] w-full object-cover object-[0_35%]"
          />
          <article class="space-y-4 p-4">
            <div class="h2">Gabriel Lugo</div>
            <p class="opacity-60">
              Gabriel Lugo is a senior in Computer Science at ODU, with a
              interest in systems programming. He loves watching anime and
              designing games in his free time.
            </p>
          </article>
        </div>
        <div
          class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y divide- overflow-hidden"
        >
          <img
            src="/img/mem/jillian_cequeria.jpg"
            alt="jillian_cequeria"
            class="aspect-[12/9] w-full object-cover object-[0_40%]"
          />
          <article class="space-y-4 p-4">
            <div class="h2">Jillian Cequeria</div>
            <p class="opacity-60">
              Jillian Cequeria is working on a Computer Science degree at Old
              Dominion University, and hopes to work in the gaming field in the
              future.
            </p>
          </article>
        </div>
        <div
          class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y divide- overflow-hidden"
        >
          <img
            src="/img/mem/brandon_thomas.jpeg"
            alt="brandon_thomas"
            class="aspect-[12/9] w-full object-cover object-[0_60%]"
          />
          <article class="space-y-4 p-4">
            <div class="h2">Brandon Thomas</div>
            <p class="opacity-60">
              Brandon has earned an associates degree at TCC and is working
              towards finishing his computer science/data science degree at ODU.
            </p>
          </article>
        </div>
        <div
          class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y divide- overflow-hidden"
        >
          <img
            src="/img/mem/jacob_thompson.png"
            alt="jacob_thompson"
            class="aspect-[12/9] w-full object-cover object-[0_50%]"
          />
          <article class="space-y-4 p-4">
            <div class="h2">Jacob Thompson</div>
            <p class="opacity-60">
              Jacob Thompson is a Junior at Old Dominion University purusing
              both a Bachelors degree in Computer Science and Big Data
              Analytics. He is also the Manager and Team Captain of the Varsity
              Smash Brothers team as a part of Old Domnion Universities Esports
              Program.
            </p>
          </article>
        </div>
        <div
          class="card preset-filled-surface-50-950 border-surface-200-800 divide-surface-200-800 block divide-y divide- overflow-hidden"
        >
          <img
            src="/img/mem/bryan_baker.png"
            alt="bryan_baker"
            class="aspect-[12/9] w-full object-cover object-[0_25%]"
          />
          <article class="space-y-4 p-4">
            <div class="h2">Bryan Baker</div>
            <p class="opacity-60">
              Bryan Baker is an aspiring programmer, currently working on
              completing his senior year of his Computer Science Bachelors
              program at Old Dominion University.
            </p>
          </article>
        </div>
      </div>
    </article>
  </div>
</div>

<style>
</style>
