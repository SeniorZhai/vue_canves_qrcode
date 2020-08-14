<template>
  <div class="hello">
    <canvas id="canvas" />
  </div>
</template>

<script>
import qrcode from 'qrcode';
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  mounted(){
      let canvas = document.getElementById('canvas');
      qrcode.toCanvas(canvas,"mixin",error=>{
        console.log(error)
      })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
