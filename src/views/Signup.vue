<script>
import SignupForm from "../components/Signup-Form.vue";

export default {
  components: {
    SignupForm,
  },
};
</script>

<template>
  <section class="flex justify-center items-center flex-col min-h-screen">
    <h1 class="my-10 text-4xl font-bold">Register a free account</h1>

    <SignupForm />
  </section>
</template>
