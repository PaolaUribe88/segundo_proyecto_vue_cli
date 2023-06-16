<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    
    <hr>
    <TwoWay nombre="Inserte Texto"></TwoWay>
    <hr>
    <ifDirective></ifDirective>
    <hr>
    <ForDirective></ForDirective>

    <p id="parrafoInfo">{{ info }}</p>
    <input id="inputMsj" type="text" v-bind:value="mensaje">
    <p>Imagen Web</p>
    <img v-bind:src="imgWeb">
    <br>
    <p>Imagen Local</p>
    <img v-bind:src="rutaImg">
    
  </div>
</template>

<script>
//importamos HelloWorld desde la siguiente ruta
import HelloWorld from './components/HelloWorld.vue';
import TwoWay from './components/TwoWay.vue';
import ifDirective from './components/IfDirective.vue';
import ForDirective from './components/ForDirective.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    TwoWay,
    ifDirective,
    ForDirective

},
  data: function () {
    return{
      info: 'One Way Data Binding',
      mensaje: 'Esto Tambien se ve, usando directiva v-bind',
      //EL REQUIRE PERMITE TRAER LA IMG, PARA QUE LA FUNCION OBTENGA LA INFORMACION
      rutaImg: require('./assets/img.jpg'),
      imgWeb: 'https://media.vandalsports.com/i/1706x960/7-2020/202071155927_1.jpg.webp',
      nombImg: 'Piratas del Caribe'

    }
  },
  methods:{

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#parrafoInfo{
  background-color: blueviolet;
  color: aliceblue;
  font-size: 30px;
}
#inputMsj{
  background-color: blue;
  color: aliceblue;
  font-size: 20px;
}
</style>
