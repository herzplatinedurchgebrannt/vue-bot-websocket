<template>
  <div class="account">
    <ul>
      <img height="50" :src= imgSrc />
      <li><h1> {{ artist }}</h1></li>
      <li><h1> {{ song }} </h1></li>  
      <li><h1> {{ email }} </h1></li>
      <li><h1> {{ state }} </h1></li>
      <li><h1> {{ playedSongs }} </h1></li>
      <li><h1> 30s </h1></li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'AccountSingle',
  props: {
    artist: String,
    song: String,
    email: String,
    state: String,
    imgSrc: String,
    playedSongs: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>



.account {
  background-color: lightblue;
}

h1 {
  margin: 7px;
}


h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
  text-align: left;
  display: inline-block;
}
li {
  display: inline-block;
  margin: 0 10px;
  padding-top: 150;
  text-align: left;
  
}
a {
  color: #42b983;
}
</style>
