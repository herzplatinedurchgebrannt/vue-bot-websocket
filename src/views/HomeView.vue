<template>
  <div class="home">
    <keep-alive>
    <AccountTable />
    </keep-alive>
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
