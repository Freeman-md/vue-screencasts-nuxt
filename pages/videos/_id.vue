<template>
  <div>
    <nuxt-child :video="video" />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: '',
      titleTemplate: `%s ${this.video.title} - Vue Screencasts`
    }
  },
  async asyncData({ $axios, params }) {
    
    let response = await $axios.get(`/meals/${params.id}`)
    const video = response.data

    return {
      video
    }
  }
}
</script>

<style>

</style>