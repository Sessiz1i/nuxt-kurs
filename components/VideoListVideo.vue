<template>
  <v-card width="340px" hover class="ma-2">
    <!--:to="{name:'video-watch',params:{id:video.id}}"-->
    <!--    <v-img :src="video"/>-->
    <v-card-title>{{ video.name }}</v-card-title>
    <!--    <v-card-text>
          <div class="green&#45;&#45;text" v-if="isPlayed(video.id)">
                  <font-awasome-icon icon="check" />Played
                </div>
        </v-card-text>
        <v-card-actions>
              <span v-for="tag_id in video.tag_ids" :key="`${video.id}-${tag_id}`">
                <v-btn color="green lighten-2" class="mr-2" small @mousedown.stop :to="{name:'tag',params:{id:tag_id}}">
                  {{ getTag(tag_id).name }}
                </v-btn>
              </span>
            </v-card-actions>-->
  </v-card>
</template>

<script>
export default {
  name: 'VideoListVideo',
  props: ['video']
}
</script>

<style scoped>

</style>
