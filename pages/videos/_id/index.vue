<template>
  <div>
    <h4>We are in video {{ video ? video.title : '' }}</h4>
    <nuxt-link :to="`/videos/${video ? video.id : ''}/edit`">
      <button>Edit</button>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Watch'
  },
  props: [
    'video'
  ]
}
</script>

<style>

</style>