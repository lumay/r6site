<template>
  <div id="switcher">
    <div v-bind:class="background">
      <div class="imglol">
      <div v-bind:class="classbutton" v-on:click="onClick">
        <img v-bind:src="imageLink"/>
      </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Switcher',
  data () {
    return {
      imgclass: 'def',
      imageLink: 'https://cdn.discordapp.com/attachments/87876057021026304/440323587669360651/def.png',
      background: 'bodyblue',
      classbutton : 'ctrl-standard typ-subhed fx-bubbleUpBlue',
      text: 'Le role de la defense, ut hoc insidiarum genere Galli periret avunculus, ne eum ut praepotens acueret in fiduciam exitiosa coeptantem. verum navata est opera diligens hocque dilato Eusebius praepositus cubiculi missus est Cabillona aurum secum perferens, quo per turbulentos seditionum concitores occultius distributo et tumor consenuit militum et salus est in tuto locata praefecti. deinde cibo abunde perlato castra die praedicto sunt mota.'
    } },
  methods: {
    onClick: function () {
      if (this.imgclass === 'def') {
        this.imageLink='https://cdn.discordapp.com/attachments/87876057021026304/440323585744175114/atk.png';
        this.imgclass = 'atk';
        this.background = 'bodyorange';
        this.classbutton = 'ctrl-standard typ-subhed fx-bubbleUp';
        this.text = 'Le role de lattaque, ut hoc insidiarum genere Galli periret avunculus, ne eum ut praepotens acueret in fiduciam exitiosa coeptantem. verum navata est opera diligens hocque dilato Eusebius praepositus cubiculi missus est Cabillona aurum secum perferens, quo per turbulentos seditionum concitores occultius distributo et tumor consenuit militum et salus est in tuto locata praefecti. deinde cibo abunde perlato castra die praedicto sunt mota.'
      }
      else {
        this.imageLink='https://cdn.discordapp.com/attachments/87876057021026304/440323587669360651/def.png';
        this.imgclass = 'def';
        this.classbutton = 'ctrl-standard typ-subhed fx-bubbleUpBlue';
        this.background = 'bodyblue';
        this.text = 'Le role de la defense, ut hoc insidiarum genere Galli periret avunculus, ne eum ut praepotens acueret in fiduciam exitiosa coeptantem. verum navata est opera diligens hocque dilato Eusebius praepositus cubiculi missus est Cabillona aurum secum perferens, quo per turbulentos seditionum concitores occultius distributo et tumor consenuit militum et salus est in tuto locata praefecti. deinde cibo abunde perlato castra die praedicto sunt mota.'
      }
    }
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #switcher {
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

  .container {
    height: 60px;
    width: 60px;
    margin: auto;
  }
  .container > * {
    width: 60px;
  }
  .typ-subhed {
    font-family: 'Oswald', sans-serif;
    font-size: 18px;
    line-height: 20px;
    letter-spacing: 0;
  }
  .ctrl-standard.fx-bubbleUp {
    color: #FFA500;
    border-color: #FFA500;
  }
  .ctrl-standard.fx-bubbleUp::after {
    center: auto;
    background: #FFA500;
  }
  .ctrl-standard.fx-bubbleUpBlue::after {
    center: auto;
    background: #00bfff;
  }
  .ctrl- {

  }
  [class*="ctrl-"] {

  }
  [class*="ctrl-"][class*="fx-"]:hover, [class*="ctrl-"][class*="fx-"].active {
    color: #231f20;
  }
  [class*="ctrl-"][class*="fx-"].is-reversed {
    color: #231f20;
  }
  [class*="fx-"], [class*="fx-"]:hover {
    transition: color 0.5s ease-in-out;
  }
  [class*="fx-"]:not(.fx-dyna) {
    position: relative;
    z-index: 1;
    transition-delay: 0.2s !important;
    overflow: hidden;
  }
  [class*="fx-"]:not(.fx-dyna)::after, [class*="fx-"]:not(.fx-dyna)::before {
    content: "";
    display: block;
    position: absolute;
    z-index: -1;
  }
  [class*="fx-bubble"]::after {
    transition: height 0.6s ease-in-out;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    height: 0;
    width: 100%;
  }
  [class*="fx-bubble"]:hover::after, [class*="fx-bubble"].active::after {
    transition: height 1.5s ease-in-out;
    height: 300%;
  }
  [class*="fx-bubble"]:disabled:hover::after {
    height: 10%;
  }
</style>
