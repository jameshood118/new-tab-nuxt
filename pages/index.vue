<template>
  <div class="container mx-auto">
    <div class="grid grid-cols-1 gap-4 p-4 md:grid-cols-1">
      <div class="p-4 rounded">
      <SearchBar />
      </div>
      <div class="p-4 rounded">
      <div class="flex items-center justify-center space-x-4">
      <AppIcon name="facebook" link="https://facebook.com" />
      <AppIcon name="youtube" link="https://youtube.com" />
      <AppIcon name="spotify" link="https://spotify.com" />
      <AppIcon name="dribbble" link="https://dribbble.com" />
      <AppIcon name="paypal" link="https://paypal.com" />
      </div>
      </div>
      <div class="p-4 rounded">
        <div class="panel">
          <button
          type="button"
          v-for="category in categories"
          :key=
          "category"
          :class="[
          'btn',
          activeTab === category ? 'text-black active underline' : ''
          ]"
          @click="setActiveTab(category)"
          >
          {{ category }}
          </button>
          <div class="container mx-auto p-4">
            <div class="grid grid-cols-4 gap-5">
              <div v-for="p in products">
              <Card :product="p" />
              </div>
            </div>
          </div>         
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const categories = [
  'Home', 'News', 'Sports', 'Money', 'Lifestyle',
  'Politics', 'Health', 'Food', 'Entertainment'
]

const activeTab = ref('Home')

const setActiveTab = (tab) => {
  activeTab.value = tab
}

if (activeTab.value == "Home") {

}
const { data: products } = await useFetch('https://fakestoreapi.com/products')

</script>

<style scoped>

</style>