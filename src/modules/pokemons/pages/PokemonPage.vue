<template>
  <section>
    <h1 class="text-3xl font-bold">
      Pokemon <small class="text-blue-500">#{{ id }}</small>
    </h1>
    <img
      :src="`https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/${id}.svg`"
      alt="Pokemon"
      class="w-[200px] h-[200px] mt-10"
      width="200"
      height="200"
    />
    <RouterLink
      class="flex w-full justify-center rounded-md bg-indigo-600 px-3 py-1.5 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600 mt-10"
      :to="{ name: 'pokemon', params: { id: id + 1 } }"
    >
      Siguiente
    </RouterLink>
  </section>
</template>

<script lang="ts" setup>
interface Props {
  id: number;
}
const props = defineProps<Props>();
</script>
