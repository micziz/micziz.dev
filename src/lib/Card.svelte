<script lang="ts">
  export let title: string;
  export let desc: string;
</script>

<div
  class="max-w-xs overflow-hidden rounded-lg border-2 hover:border-indigo-700"
>
  <div class="px-6 py-4">
    <h4
      class="mb-3 text-xl font-semibold tracking-tight text-gray-800 text-center"
    >
      {title}
    </h4>
    <p class="leading-normal text-gray-700 text-center">{desc}</p>
  </div>
</div>
