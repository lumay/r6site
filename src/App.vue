<template>
  <div id="app">
    <transition name="fade">
    <div class="wrapper"> <!-- for reasons -->
      <div class="main-content end-animation" v-bind:style="{ width: computedWidthB }" @mouseover="changeWidthB()" @mouseleave="resetWidth()">
        <button @click="changeAccueil" v-if="computedWidthB === '90%'" class="btn btn-primary">lol {{ accueil }}</button>

      </div>

      <div class="aside end-animation" v-bind:style="{ width: computedWidthO }" @mouseover="changeWidthO()" @mouseleave="resetWidth()">
      </div>

    </div>
    </transition>
    <button @click="changeAccueil" v-if="!accueil">lol {{ accueil }}</button>

    <guide v-if="!accueil" id="guide"></guide>
    <transition name="fade">
    <switcher v-if="!accueil"></switcher>
    </transition>



    <!--<div class="center"><separator></separator></div>-->
  </div>
</template>

<script>
  import Vue from 'vue'
  import BootstrapVue from 'bootstrap-vue'
  Vue.use(BootstrapVue);
  import 'bootstrap/dist/css/bootstrap.css'
  import 'bootstrap-vue/dist/bootstrap-vue.css'
  import axios from  'axios'
  import Switcher from '@/components/Switcher'
  import Separator from '@/components/Separator'
  import Guide from '@/components/Guide'

export default {
  name: 'App',
  data(){ return{
    widthB:'50%',
    widthO:'50%',
    flag:false,
    accueil:true
    } },
  computed: {
    computedWidthB: function () {
      return this.widthB;
    },
    computedWidthO: function () {
      return this.widthO;
    }
  },
  methods: {
    changeWidthB: function (event) {
      this.widthB='90%';
      this.widthO='10%';
      this.flag=true;
    },
    changeWidthO: function (event) {
      this.widthB='10%';
      this.widthO='90%';
      this.flag=false;
    },
    resetWidth: function (event) {
      this.widthB='50%';
      this.widthO='50%';
      this.flag=false;
    },
    changeAccueil: function (event) {
      this.accueil=!this.accueil;
    },

  },
  components: {Switcher,Guide},
}

</script>

<style>
  /** {*/
    /*box-sizing: border-box;*/
    /*margin: 0;*/
    /*padding: 0;*/
  /*}*/
  .fade-enter-active, .fade-leave-active {
    transition: opacity 0.7s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }
  .end-animation {
    transition: width .3s;
  }
  .main-content{
    width: 50%;
    background: url(img/r6fond.jpg);
    float: left;

    height: 100%;
    border-right:5px orange solid;
  }
  .aside{
    width: 50%;
    float: left;
    background: url(img/damn.png);

    height: 100%;
  }

  .wrapper, html, body{
    height: 100%;
  }
#app {
  font-family: 'Avenir', "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: red;
  height: 100%;
}


</style>
