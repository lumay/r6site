<template>
  <div id="api">
    <button @click="getCharacter">mabite</button>
    <div v-for="perso in persos">
      {{ perso.nom }}


    </div>
  </div>
</template>

<script>
export default {
  name: 'Api',
  data () {
    return {
      persos:[]
      } },
  methods: {
    getCharacter: function() {
      var self = this;
      axios.get('http://localhost:3000/persos')
        .then(function (response) {
          self.persos=response.data;
        })
        .catch(function (error) {
          console.log(error);
        });
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #app {
    font-family: 'Avenir', "Open Sans", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }
  .imglol {
    position: fixed;
    top: 10%;
    right: 5%;
  }
  .bodyblue {
    background: linear-gradient(to right, #189B95, #06688A);;
  }
  .bodyorange {background: linear-gradient(to left, #189B95, #06688A);}
</style>
