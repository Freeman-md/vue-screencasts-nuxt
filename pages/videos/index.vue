<template>
  <div>
    <h3>List of Videos</h3>
    <div 
      v-for="(video, index) in videos" 
      :key="index"
    >
      <nuxt-link :to="`/videos/${video.id}`">{{ video.name}}</nuxt-link>
    </div>
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
  })
}
</script>