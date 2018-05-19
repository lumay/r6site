<template>
  <div id="app">
    <div v-bind:class="background">
      <div class="imglol" v-on:click="onClick">
        <img v-bind:src="imageLink"/>
      </div>
      <p> {{text}} </p>
    </div>
    <!--<img src="./assets/logo.png">-->
    <!--<router-view/>-->
  </div>
</template>

<script>
  import Vue from 'vue'
  import BootstrapVue from 'bootstrap-vue'
  Vue.use(BootstrapVue);
  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  name: 'App',
  data(){ return{
    imgclass: 'def',
    imageLink: 'https://cdn.discordapp.com/attachments/427543667570376724/427544229984731136/chrome_2018-03-19_17-09-24.png',
    background: 'bodyblue',
    text: 'Le role de la defense, ut hoc insidiarum genere Galli periret avunculus, ne eum ut praepotens acueret in fiduciam exitiosa coeptantem. verum navata est opera diligens hocque dilato Eusebius praepositus cubiculi missus est Cabillona aurum secum perferens, quo per turbulentos seditionum concitores occultius distributo et tumor consenuit militum et salus est in tuto locata praefecti. deinde cibo abunde perlato castra die praedicto sunt mota.'
  } },
  methods: {
    onClick: function () {
      if (this.imgclass === 'def') {
        this.imageLink='https://cdn.discordapp.com/attachments/427543667570376724/427544227673669632/chrome_2018-03-19_17-09-06.png';
        this.imgclass = 'atk';
        this.background = 'bodyorange';
        this.text = 'Le role de lattaque, ut hoc insidiarum genere Galli periret avunculus, ne eum ut praepotens acueret in fiduciam exitiosa coeptantem. verum navata est opera diligens hocque dilato Eusebius praepositus cubiculi missus est Cabillona aurum secum perferens, quo per turbulentos seditionum concitores occultius distributo et tumor consenuit militum et salus est in tuto locata praefecti. deinde cibo abunde perlato castra die praedicto sunt mota.'
      }
      else {
        this.imageLink='https://cdn.discordapp.com/attachments/427543667570376724/427544229984731136/chrome_2018-03-19_17-09-24.png';
        this.imgclass = 'def';
        this.background = 'bodyblue';
        this.text = 'Le role de la defense, ut hoc insidiarum genere Galli periret avunculus, ne eum ut praepotens acueret in fiduciam exitiosa coeptantem. verum navata est opera diligens hocque dilato Eusebius praepositus cubiculi missus est Cabillona aurum secum perferens, quo per turbulentos seditionum concitores occultius distributo et tumor consenuit militum et salus est in tuto locata praefecti. deinde cibo abunde perlato castra die praedicto sunt mota.'
      }
    }
  }
}

</script>

<style>
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
