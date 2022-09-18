<template>
  <div>
    <h1>
      Edit Video {{ video.name }}
    </h1>
  </div>
</template>

<script>
export default {
  props: ['video'],
  head: { title: 'Edit' }
}
</script>

<style scoped>

</style>
