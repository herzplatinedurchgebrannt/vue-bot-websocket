<template>
<keep-alive>
  <div class="account">
    <img height="50" :src= imgSrc align="center" />
    <h1 class="bold"> {{ artist }}</h1>
    <h1> {{ song }} </h1>  
    <h1 class="bold"> {{ email }} </h1>
    <h1> {{ state }} </h1>
    <h1 class="bold"> {{ playedSongs }} Plays</h1>
  </div>
  </keep-alive>
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

.bold {
  font-weight: bold;
}

img {
  display: inline;
  width: 100px;
  height: 100px;
  
  }
h1 {
  font-size: 22px;
  font-weight: normal;
  display: inline;
  margin: 15px;
  padding: 12px;
}
.container div {
  display: inline-block;
}

.account {
  background-color: lightblue;
  padding: 10px;
  margin: 10px;
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
  text-align: center;

}


a {
  color: #42b983;
}

</style>
