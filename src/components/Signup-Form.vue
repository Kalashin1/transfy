<script>
import SubmitButton from "./Submit-Button.vue";

export default {
  data() {
    return {
      username: "",
      password: "",
    };
  },
  components: {
    SubmitButton,
  },
  methods: {
    register() {
      console.log(this.username)
      localStorage.setItem("username", this.username);
      this.$router.push('/dashboard')
    },
  },
};
</script>

<template>
  <form class="p-4" @submit.prevent="register">
    <div class="flex justify-between items-center my-4">
      <label class="mr-4">Username</label>
      <input
        type="text"
        v-model="username"
        placeholder="JohnDOe"
        class="py-2 px-16 bg-gray-200 shadow-md focus:outline-none focus:bg-zinc-600 focus:text-gray-50 rounded-2xl w-full"
      />
    </div>
    <div class="flex justify-between items-center my-4">
      <label class="mr-4">Password</label>
      <input
        type="password"
        v-model="password"
        class="py-2 px-16 bg-gray-200 shadow-md focus:outline-none focus:bg-zinc-600 focus:text-gray-50 rounded-2xl w-full"
      />
    </div>

    <div class="flex py-4 justify-center items-center my-4">
      <SubmitButton />
    </div>
  </form>
</template>
