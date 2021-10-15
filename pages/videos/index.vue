<template>
  <div>
    <h3>List of Videos</h3>
    <div 
      v-for="(videos, index) in $store.state.videos" 
      :key="index"
    >
      <nuxt-link :to="`/videos/${videos.id}`">{{ videos.title}}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Vue Screencasts - Video List'
  },
  async fetch({ $axios, store }) {
    let response = await $axios.get('/meals')
    const videos = response.data.data

    store.commit('SET_VIDEOS', videos)
  }
}
</script>