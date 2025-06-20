<template>
  <div class="input">
  <form @submit.prevent="handleSearch" class="flex items-center space-x-2">
    <input
      v-model="query"
      type="text"
      placeholder="Search the web or type a URL"
      class="rounded w-full"
    />
  </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const query = ref('')

function handleSearch() {
  if (query.value.trim()) {
    const searchUrl = `https://search.yahoo.com/search?p=${encodeURIComponent(query.value)}`
    window.location.href = searchUrl
  }
}
</script>

<style scoped>
input:focus {
  outline: none;
  border-color: #2563eb; /* Tailwind blue-600 */
}
</style>