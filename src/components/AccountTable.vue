<template>
  <!--h2>{{accounts}}</h2-->
  <div class="table">
    <h1> Account table </h1>
    <!--AccountSingle /-->
  </div>

  <li v-for="account in accounts" :key="account.message">
    <AccountSingle :artist=account.currentBand :song=account.currentTitle 
                   :email=account.email :state=account.state :imgSrc=account.currentImage 
                   :playedSongs=account.logPlayedSongs   />
  
  </li>
</template>

<script>

import AccountSingle from '@/components/AccountSingle.vue'

export default {
  name: 'AccountTable',
  props: {
  },
  components: {
    AccountSingle
  },
  data: function () {
    return {

      linki: "https://www.impuls-medien.org/wp-content/uploads/2016/04/dummy-post-square-1-2.jpg",

      time: null,
      accounts: [],
    }
  },
  mounted: function(){
    let connection = new WebSocket('ws://localhost:3000/');
    connection.onmessage = (event) => {

      console.log(event);
      // Vue data binding means you don't need any extra work to
      // update your UI. Just set the `time` and Vue will automatically
      // update the `<h2>`.
      this.accounts = JSON.parse(event.data);
    }
  },




}
</script>









<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {

  padding: 0;
}
li {

  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
