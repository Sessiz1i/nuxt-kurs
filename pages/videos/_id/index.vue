<template>
  <div v-if="video">
    <span>We are in Video {{ video.name }}</span>
    <nuxt-link :to="`/videos/${video.id}/edit`">
      <button>Edit</button>
    </nuxt-link>
  </div>
  <div v-else>
    <h1>Video Not Fount</h1>
  </div>

</template>

<script>
export default {
  props: ['video']
}
</script>

<style scoped>

</style>
