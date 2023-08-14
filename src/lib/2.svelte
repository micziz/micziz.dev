<script lang="ts">
    import Card from "./Card.svelte";

    let one = true;
    let two = false;
</script>

<h2 class="text-center text-2xl mt-20 mb-10">Projects</h2>

<div class="mb-12 grid grid-cols-3 space-x-6 place-items-center">
    {#if one}
        <a href="https://quiz.micziz.dev">
            <Card title="Quizzicle" desc="A quiz game built with svetekit and typescript" />
        </a>
        <a href="https://huff.micziz.dev">
            <Card title="Hufferpuff" desc="A search engine buit in typescript with the DuckDuckGo API"/>
        </a>
        <a href="https://bse.micziz.dev">
            <Card title="BSE" desc="A search engine built with typescript just for searching basketball players" />
        </a>
    {:else if two}
        <a href="https://github.com/setsojs/setso">
            <Card title="Setso" desc="A library to compile md to html in a clean way" />
        </a>
        <a href="https://pkdx.micziz.dev">
            <Card title="PKDX" desc="Free pokedex with no ads built in svelte"/>
        </a>
        <a href="https://gtf.micziz.dev">
            <Card title="Gtf" desc="A fun game where you need to guess the flag!"/>
        </a>
    {:else}
        <p>There was an error</p>
    {/if}
</div>

<div class="flex flex-col items-center justify-center mb-10">
    <div class="inline-block">
        <button class="mr-10 text-center h-10 px-5 text-indigo-700 transition-colors duration-150 border border-indigo-500 rounded-lg focus:shadow-outline hover:bg-indigo-500 hover:text-indigo-100" on:click={() => {
          one = true;
          two = false;
        }}>1</button>
        <button class="mr-10 text-center h-10 px-5 text-indigo-700 transition-colors duration-150 border border-indigo-500 rounded-lg focus:shadow-outline hover:bg-indigo-500 hover:text-indigo-100" on:click={() => {
          one = false;
          two = true;
        }}>2</button>
    </div> 
</div>

