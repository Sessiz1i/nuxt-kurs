<template>
  <div>
    <nuxt-child/>
    <h1>Videos</h1>
    <div v-for="video in $store.state.videos" :key="video.id">
      <nuxt-link :to="`/videos/${video.id}`">{{ video.name }}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Video List'
  },
  async fetch ({ $axios, store }) {
    let { data: videos } = await $axios.get('/videos')
    store.commit('SET_VIDEOS', videos)
  }
}
</script>

<style scoped>

</style>
