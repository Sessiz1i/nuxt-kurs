<template>
  <div class="home">

    <div class="display-4 ma-4 d-flex justify-center">
      All Videos
    </div>

    <div class="d-flex flex-wrap">
      <div v-for="video in videos" :key="video.name">
        <VideoListVideo :video="video"/>
      </div>
    </div>

  </div>
</template>

<script>
import VideoListVideo from '~/components/VideoListVideo'
export default {
  head: {
    title: 'Ana Sayfa'
  },
  components:{
    VideoListVideo
  },
  async asyncData ({ $axios }) {
    let { data: videos } = await $axios.get('/videos')
    return {
      videos
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
