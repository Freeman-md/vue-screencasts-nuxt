<template>
  <div>
    <h4>We are in video {{ video ? video.name : '' }}</h4>
    <nuxt-link :to="`/videos/${video.id}/edit`">
      <button>Edit</button>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  props: [
    'video'
  ]
}
</script>

<style>

</style>