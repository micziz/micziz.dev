<script lang="ts">
  import One from './lib/1.svelte'
  import Two from './lib/2.svelte'
  import Three from './lib/3.svelte'
  import { fade, slide } from "svelte/transition";

  const sleep = (ms: number) => new Promise((r) => setTimeout(r, ms));

  let one = true;
  let two = false;
  let three = false;
</script>

<main class="h-screen">
  <div class="flex h-screen flex-col items-center justify-center">
    {#if one}
      <div in:fade={{ duration: 1000 }} out:fade={{ duration: 2000 }}>
        <One/>
      </div>
    {:else if two}
      <div in:fade={{ duration: 1000 }} out:fade={{ duration: 2000 }}>
        <Two/>
      </div>
    {:else if three}
      <div in:fade={{ duration: 1000 }} out:fade={{ duration: 2000 }}>
        <Three/>
      </div>
    {/if}
    <div class="inline-block">
      <button class="mr-10 text-center h-10 px-5 text-indigo-700 transition-colors duration-150 border border-indigo-500 rounded-lg focus:shadow-outline hover:bg-indigo-500 hover:text-indigo-100" on:click={async () => {
        two = false;
        three = false;
        await sleep(2000)
        one = true;
      }}>Home</button>
      <button class="mr-10 text-center h-10 px-5 text-indigo-700 transition-colors duration-150 border border-indigo-500 rounded-lg focus:shadow-outline hover:bg-indigo-500 hover:text-indigo-100" on:click={async () => {
        one = false;
        three = false;
        await sleep(2000)
        two = true;
      }}>Projects</button>
      <button class="h-10 text-center px-5 text-indigo-700 transition-colors duration-150 border border-indigo-500 rounded-lg focus:shadow-outline hover:bg-indigo-500 hover:text-indigo-100" on:click={async () => {
        one = false;
        two = false;
        await sleep(2000)
        three = true;
      }}>Socials</button>
    </div> 
  </div>
</main>
