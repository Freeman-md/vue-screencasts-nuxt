<template>
  <div>
    <h3>List of Videos</h3>
    <div 
      v-for="(meal, index) in meals" 
      :key="index"
    >
      <nuxt-link :to="`/videos/${meal.id}`">{{ meal.title}}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    let response = await $axios.get('/meals')
    const meals = response.data.data

    return {
      meals
    }
  }
}
</script>