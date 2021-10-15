<template>
  <div>
    <h4>We are in videos {{ video ? video.name : '' }}</h4>
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