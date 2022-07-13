<script>
export default {
  props: ["text", "num"]
}
</script>

<template>
  <div class="rounded-md shadow-md bg-gray-100 text-gray-900 md:px-6 px-3 py-4 lg:m-4 m-2 lg:w-44 w-full">
    <h1 class="font-bold text-xl sm:text-2xl">{{ text }}</h1>
    <div class="flex justify-between items-center my-4 space-x-2">
      <i class="fas text-3xl fa-balance-scale text-red-500"></i>
      <h3 class="sm:text-lg font-bold">${{ num }}</h3>
    </div>
  </div>
</template>