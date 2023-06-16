<template>
    <div id="App2">
        <h1>Two Way Data Binding</h1>
        <input type="text" v-model="nombre">
        <h2 id="nombreCont">{{ nombre }}</h2>
        <button v-on:click="cambiarNombre">Cambia el Modelo</button>
    </div>
</template>
<script>
export default{
   name:'Two way Component',
    data : function(){
        return{
            nombre:'',
        }

    },
    methods:{
        cambiarNombre: function(){
            this.nombre='Cambiamos el modelo de nombre'
        }

    }

}

</script>

<style scoped>
#App2{
    background-color: aquamarine;
}
#nombreCont{
    color: rgb(222, 58, 8);
    background-color: rgb(46, 226, 43);
    font-size: 50px;
}
</style>