<template>
  <div class="or-spacer">
    <div class="mask"></div>
    <!--<span><i>or</i></span>-->
  </div>
</template>

<script>
export default {
  name: 'Separator',
  data() {
    return {}
  },
  methods: {},
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
  .or-spacer {
    margin-top:100px;
    margin-left:100px;
    width:800px;
    position:static;
  }
  .or-spacer .mask {
    overflow:hidden;
    height:20px;
  }
  .or-spacer .mask:after {
    content:'';
    display:block;
    margin:-25px auto 0;
    width:100%;
    height:25px;
    border-radius:125px / 12px;
    box-shadow:0 0 16px black;
  }
  .or-spacer span {
    width:50px;
    height:50px;
    position:absolute;
    bottom:100%;
    margin-bottom:-25px;
    left:50%;
    margin-left:-25px;
    border-radius:100%;
    box-shadow:0 2px 4px #999;
    background:white;
  }
  .or-spacer span i {
    position:absolute;
    top:4px;
    bottom:4px;
    left:4px;
    right:4px;
    border-radius:100%;
    border:1px dashed #aaa;
    text-align:center;
    line-height:40px;
    font-style:normal;
    color:#999;
  }

</style>
