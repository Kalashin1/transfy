<script>
  export default {
    props: ["text"]
  };
</script>


<template>
  <button class="px-8 flex text-lg justify-between items-center w-full my-4 rounded-md bg-gray-200 text-gray-900 font-bold shadow-md py-2">
    {{ text }}
    <i class="fas fa-arrow-right text-lg"></i>
  </button>
</template>