<script>
export default {
  data() {
    return {
      transactions: [
        {
          name: 'John Doe',
          id: 1,
          amount: 300,
          status: 'approved'
        },
        {
          name: 'Joa Felix',
          id: 2,
          amount: 250,
          status: 'approved'
        },
        {
          name: 'Mirrian Webstar',
          id: 3,
          amount: 150,
          status: 'approved'
        },
      ]
    }
  }
}
</script>

<template>
<div class="py-8 rounded-lg overflow-x-scroll">
  <table class="border bg-gray-100 rounded-lg w-ful shadow-md w-full">
    <thead>
      <th class="py-2 px-6 text-lg font-bold">Order Id</th>
      <th class="py-2 px-6 text-lg font-bold">Order Name</th>
      <th class="py-2 px-6 text-lg font-bold">Amount</th>
      <th class="py-2 px-6 text-lg font-bold">Status</th>
      <th class="py-2 px-6 text-lg font-bold">Action</th>
    </thead>
    <tbody class="md:px-6 md:py-4">
      <template v-for="(transaction) in transactions" :key="transaction.id">
        <tr class="border-t border-gray-300 px-6">
          <td class="py-4 text-center px-6">{{ transaction.id }}</td>
          <td class="py-4 text-center px-6">{{ transaction.name }}</td>
          <td class="py-4 text-center px-6">${{ transaction.amount }}</td>
          <td class="py-4 text-center px-6">
            <span class="py-2 px-4 bg-green-700 text-gray-50 rounded-lg">{{ transaction.status }}</span>
          </td>
          <td class="py-4 px-6 space-x-4 text-center">
            <i class="fas fa-trash text-red-600 text-lg"></i>
            <i class="fas fa-edit text-blue-600 text-lg"></i>
          </td>
      </tr>
      </template>
     
    </tbody>
  </table>
</div>
</template>