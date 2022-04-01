<template>
  <div class="create">
    <NewComponent />
  </div>
</template>

<script>
// @ is an alias to /src
import NewComponent from '@/components/NewComponent.vue'

export default {
  name: 'CreatorView',
  components: {
    NewComponent
  }
}
</script>
