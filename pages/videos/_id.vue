<template>
  <div>
    <nuxt-child :video="video" />
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  head() {
    return {
      title: '',
      titleTemplate: `%s ${this.video.title} - Vue Screencasts`
    }
  },
  async fetch({ $axios, params, store }) {
    
    let response = await $axios.get(`/meals/${params.id}`)
    const video = response.data

    store.commit('SET_CURRENT_VIDEO', video)
  },
  computed: {
    ...mapState({
      video: 'currentVideo'
    })
  }
}
</script>

<style>

</style>