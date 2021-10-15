<template>
  <div>
    <nuxt-child :video="meal" />
  </div>
</template>

<script>
export default {
  async asyncData({ $axios, params }) {
    
    let response = await $axios.get(`/meals/${params.id}`)
    const meal = response.data

    return {
      meal
    }
  }
}
</script>

<style>

</style>