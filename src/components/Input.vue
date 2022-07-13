<script>
export default {
  props: ["type", "placeholder", "label"],
};
</script>

<template>
  <div class="flex justify-between items-center my-4">
    <label class="mr-4">{{ label }}</label>
    <input
      :type="type"
      :placeholder="placeholder"
      class="py-2 px-16 bg-gray-200 shadow-md focus:outline-none focus:bg-zinc-600 focus:text-gray-50 rounded-2xl w-full"
    />
  </div>
</template>
