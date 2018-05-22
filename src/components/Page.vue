<template>

  <div id="page" class="">
<link href="https://fonts.googleapis.com/css?family=Raleway:200" rel="stylesheet">
  <button v-on:click="Langue('en')">{{ textfr }}</button>
  <div v-if="language==='zz'">
<h1 align=center>BLUEPAW.IO</h1>
<h2 align=center>SELECTIONNEZ UN JEU</h2>
  <div class="table-responsive">
  <table align=center class="table">
    <tr>


  <td>
            <div class="[ c-example__tilt ] js-tilt" js-tilt-perspective="300" js-tilt-speed="40000" js-tilt-max="25" style="will-change: transform; transform: perspective(300px) rotateX(0deg) rotateY(0deg);">
                <div class="text-tilt">jeu 1</div>
            </div>
  </td>
  <td>
  <div class="[ c-example__tilt ] js-tilt" data-tilt-perspective="300" data-tilt-speed="400" data-tilt-max="25" style="will-change: transform; transform: perspective(300px) rotateX(0deg) rotateY(0deg);">
                <div class="text-tilt">jeu 2</div>
            </div>
  </td>
  <td>
  <div class="[ c-example__tilt ] js-tilt" data-tilt-perspective="300" data-tilt-speed="400" data-tilt-max="25" style="will-change: transform; transform: perspective(300px) rotateX(0deg) rotateY(0deg);">
                <div class="text-tilt">jeu 3</div>
            </div>
  </td>
  <td>
  <div class="[ c-example__tilt ] js-tilt" data-tilt-perspective="300" data-tilt-speed="400" data-tilt-max="25" style="will-change: transform; transform: perspective(300px) rotateX(0deg) rotateY(0deg);">
                <div class="text-tilt">jeu 4</div>
            </div>
  </td>

    </tr>
   </table>
  </div>
  </div>
  </div>
</template>

<script>

export default {
  name: 'Page',
  data() {
    return {
      textfr: 'Passez en anglais',
      texten: 'Switch to english',
      language: 'fr',
    }
  },
  methods: {
    Langue (lang) {
      if (lang === 'fr') {
        this.language='fr';
      }
      if (lang === 'en') {
        this.language='en';
      }
    }},
}

</script>

<style>
  body {

  }
#app {
  font-family: 'Avenir', "Open Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: dimgrey;
}
  body {
    /*background-color: #189B95;*/
    background: linear-gradient(to left, #189B95, #06688A);
    font-family: 'Raleway', sans-serif;
  }
  h1, h2, h3, h4 {margin: 1em 0 .5em; line-height: 1.25; color:white}
  h1 {font-size: 2em;}
  h2 {font-size: 1.5em;}
  h3 {font-size: 1.2em;}
  .table {width: 45%; border: 1px solid white;}
  th, td {
    padding: 15px;
    text-align: left;
  }

  .c-example__tilt {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    display: block;
    background-color: #3ee0d6;

    box-shadow: 0 3px 47px rgba(0, 0, 0, 0.2);
    -webkit-transform-style: preserve-3d;
    transform-style: preserve-3d;
    -webkit-transform: perspective(300px);
    transform: perspective(300px); }
  .c-example__demo {
    -webkit-box-flex: 0;
    -ms-flex: 0 1 15%;
    flex: 0 1 15%;
    min-width: 100px;
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    justify-content: center; }
  .c-example__tilt-inner {
    -webkit-transform: translateZ(50px) translateY(-50%) translateX(-50%);
    transform: translateZ(50px) translateY(-50%) translateX(-50%);
    position: absolute;
    top: 50%;
    left: 50%;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: white;
    box-shadow: 0 0 50px 0 rgba(51, 51, 51, 0.3); }
  .text-tilt{
    -webkit-transform: translateZ(75px) translateY(-50%) translateX(-50%);
    transform: translateZ(75px) translateY(-50%) translateX(-50%);
    position: absolute;
    top: 50%;
    left: 50%;

  }
</style>
