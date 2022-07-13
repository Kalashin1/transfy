<script>
import Sidebar from '../components/Sidebar.vue'
import TransactionTable from '../components/Transaction-Table.vue';
import TransferButton from '../components/Transfer-Button.vue';
import CardBalance from '../components/Card-Balance.vue';
import Navbar from '../components/Navbar.vue';

export default {
  data() {
    return {
      showNav: true,
    }
  },
  components: { 
    Sidebar,
    TransactionTable,
    TransferButton,
    CardBalance,
    Navbar
  },
  methods: {
    toogleNav() {
      this.showNav = !this.showNav;
    }
  }
}
</script>

<template>
<section class="grid relative md:grid-cols-5 bg-gray-50 body-text">
  <div class="grid col-span-4 w-full min-h-screen fixed top-0 z-50 lg:relative lg:col-span-1" v-if="showNav">
    <Sidebar @toggleNav="toogleNav" />
  </div>
  <div class="grid col-span-5 lg:col-span-4">
    <Navbar @toggleNav="toogleNav" />
    <div class="py-4 my-4 px-4">
      <div class="flex flex-col lg:flex-row my-2">
        <CardBalance text="Balance" num="300" />
        <CardBalance text="Transfers" num="80" />
        <CardBalance text="Utilities" num="40" />
        <CardBalance text="Bills" num="20" />
      </div>
      <hr />
      <div class="md:p-4">
        <TransferButton text="Transfer" />
        <TransferButton text="Utility" />
        <TransferButton text="Deposit" />
      </div>
    </div>
    <hr />
    <div class="md:p-4 overflow-x-scroll">
      <TransactionTable />
    </div>
  </div>
</section>
</template>