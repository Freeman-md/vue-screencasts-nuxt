<template>
  <div>
    <nuxt-child :video="video" />
  </div>
</template>

<script>
export default {
  data: () => ({
    videos: [
      {
        id: '10',
        name: 'Intro to Nuxt JS'
      },
      {
        id: '11',
        name: 'Intro to Next JS'
      },
      {
        id: '12',
        name: 'Intro to Vue JS'
      }
    ]
  }),
  computed: {
    video() {
      return this.videos.find(v => v.id == this.$route.params.id)
    }
  }
}
</script>

<style>

</style>