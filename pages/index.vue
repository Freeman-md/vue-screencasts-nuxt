<template>
  <div class="home">
    <div class="justify-center display-4 ma-4 d-flex">
      All Videos
    </div>

    <div class="flex-wrap d-flex">
      <div 
        v-for="(video, index) in videos" 
        :key="index">
        {{ video.title }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  async asyncData({ $axios }) {
    let response = await $axios.get('/meals')
    const videos = response.data.data

    return {
      videos
    }
  },
}
</script>
