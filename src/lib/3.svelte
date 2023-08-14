<script>
  import Card from "./Card.svelte";
</script>

<h2 class="text-center text-2xl my-20">Socials</h2>

<div class="mb-12 grid grid-cols-3 space-x-6 place-items-center">
    <a href="https://github.com/micziz">
        <Card title="Github" desc="Where all my projects code is. Check it out!" />
    </a>
    <a href="https://twitter.com/@micziz69">
        <Card title="X (Formerly twitter)" desc="I post sometimes on there. Mostly coding stuff" />
    </a>
    <a href="https://blog.micziz.dev">
        <Card title="Blog" desc="Still a WIP, but i will write articles and have a changelog" />
    </a>
</div>