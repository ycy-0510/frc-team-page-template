<template>
  <div>
    <h2 class="text-3xl font-bold mb-4">Contact Us</h2>
    <form class="max-w-md mx-auto bg-gray-100 p-6 rounded shadow">
      <div class="mb-4">
        <label class="block mb-2">Name</label>
        <input type="text" class="w-full p-2 border hover:border-sky-500 rounded" />
      </div>
      <div class="mb-4">
        <label class="block mb-2">Email</label>
        <input type="email" class="w-full p-2 border hover:border-sky-500 rounded" />
      </div>
      <div class="mb-4">
        <label class="block mb-2">Message</label>
        <textarea class="w-full p-2 border hover:border-sky-500 rounded"></textarea>
      </div>
      <button type="submit" class="bg-sky-500 text-white px-4 py-2 rounded hover:bg-sky-400">
        Send
      </button>
    </form>
  </div>
</template>

<script setup lang="ts">
</script>