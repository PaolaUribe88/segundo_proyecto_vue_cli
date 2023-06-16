<template>
    <div id="directivaFor">
        <h1>Esto es un For</h1>
        <section> 
            <h1>Mis conocimientos en programación web son:</h1> 
            <div class="container_skill"> 
                <ul> 
                    <li v-for="Habilidad in skills" :key="Habilidad">{{Habilidad}}</li> 
                </ul> 
                <input type="text" v-model="skill"> 
                <button v-on:click="addSkill" :disabled="skill ==''">Agregar skill</button> 
                <button v-on:click="deleteSkill">Quitar Skill</button>
            </div> 
        </section>
    </div>
</template>
<script>
export default { 
    name:"For-component", 
    data: function(){ 
        return { 
            skills:['HTML','CSS','JS'], 
            skill:"", 
        } 
    }, 
    methods:{ 
        addSkill: function(){ //agregar una nueva skill 
            this.skills.push(this.skill) 
            //limpiar input 
            this.skill = "" 
        }, 
        deleteSkill: function(){
            this.skills.pop(this.skill)
        }
    } 
}
</script>
<style scoped>
#directivaFor{
    background-color: black;
    color: bisque;
    text-align: left;
}
</style>