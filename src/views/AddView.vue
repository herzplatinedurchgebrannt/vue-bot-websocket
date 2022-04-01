<template>
  <div class="add">
    <h1>Add song to playlist</h1>
    <HelloWorld />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'AddView',
  components: {
    HelloWorld
  }
}
</script>