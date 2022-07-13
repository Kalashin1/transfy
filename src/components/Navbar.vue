<script>
export default {
  data() {
    return {
      username: localStorage.getItem('username')
    }
  }
}
</script>

<template>
  <nav class="bg-gray-200 py-2 flex relative z-30 justify-between items-center">
    <div class="flex justify-end items-center px-4">
      <button @click="$emit('toggleNav')">
        <i class="fas fa-bars"></i>
      </button>
    </div>
    <div class="p-2">
      <h3>{{ username }}</h3>
    </div>
  </nav>
</template>
