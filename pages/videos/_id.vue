<template>
  <div>
    <nuxt-child :video="video"/>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {

  head () {
    return {
      titleTemplate: `%s ${this.video.name} - Çizgi Albüm`
    }
  },
  computed: {
    ...mapState({
      video: 'currentVideo'
    })
  },
  async fetch ({ $axios, params, store }) {
    const { data: video } = await $axios.get(`/videos/${params.id}`)
    store.commit('SET_CURRENT_VIDEO', video)
  }
}
</script>

<style scoped>

</style>
