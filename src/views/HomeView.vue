<template>
  <div class="home">
    <AccountTable />
  </div>
</template>

<script>
// @ is an alias to /src
import AccountTable from '@/components/AccountTable.vue'

export default {
  name: 'HomeView',
  components: {
    AccountTable
  }
}
</script>
