<template>
  <div>
    Editing {{ video ? video.name : '' }}
    <nuxt-link :to="`/videos/${video.id}`">
      <button>Go back to show</button>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Edit'
  },
  props: ['video']
}
</script>

<style>

</style>