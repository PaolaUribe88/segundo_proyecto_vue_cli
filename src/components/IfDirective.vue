<template>
    <div id="ifDirective">
        <h1>Aqui Utilizamos un IF</h1>
         <h2>Contador de likes {{likes}}</h2> 
            <div v-if="likes === 0">No hay likes</div> 
            <div v-else-if="likes < 10">Vamos por los 10 likes</div> 
            <div v-else-if="likes < 20">Vamos por los 20 likes</div> 
            <div v-else>Eres una estrella de los likes</div> 
            <button id="btnLikes" v-on:click="addLike">Agregar</button>
            <button id="btnLikes" v-on:click="removeLike">Remover</button>
    </div>

</template>

<script>
    export default { 
        name:"If-component", 
        data: function(){ 
            return { 
                likes:0, 
            } 
        }, methods:{ 
            addLike(){
                this.likes++;
            }, 
            removeLike(){ 
                if(this.likes> 0){ 
                    this.likes--; 
                } 
            } 
        } 
    }
</script>
<style scoped>
#ifDirective{
    background-color: cornflowerblue;
}
#btnLikes{
    background-color: rgb(30, 6, 170);
    color: aliceblue;
    border-radius: 20px;
    font-size: 20px;
}
</style>