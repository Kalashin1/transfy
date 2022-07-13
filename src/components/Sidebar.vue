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
  <div class="border-r bg-zinc-600 py-4 min-h-screen">
    <div class="flex justify-end items-center px-4 lg:hidden">
      <button @click="$emit('toggleNav')">
        <i class="fas fa-times-circle text-gray-50"></i>
      </button>
    </div>
    <div class="flex justify-start items-center flex-col my-4">
      <div class="rounded-full p-4 text-center flex items-center justify-center h-20 w-20 text-4xl font-bold bg-slate-50">
        K
      </div>

      <h1 class="text-2xl my-4 font-bold text-slate-50">{{ username }}</h1>
    </div>

    <nav class="mt-auto">
      <ul>
        <li class="flex bg-gray-50 py-4 justify-evenly border-b border-zinc-600 items-center">
          <i class="fas fa-home"></i>
          <a href="dashboard" class="text-md text-lg font-bold">Dashboard</a></li>
        <li class="flex bg-gray-50 py-4 justify-evenly items-center border-b border-zinc-600">
          <i class="fas fa-credit-card"></i>
          <a href="transactions" class="text-md text-lg font-bold">Transaction</a></li>
        <li class="flex bg-gray-50 py-4 justify-evenly items-center border-b border-zinc-600">
          <i class="fas fa-automobile"></i>
          <a href="dashboard" class="text-md text-lg font-bold">Setting</a></li>
      </ul>
    </nav>
  </div>
</template>