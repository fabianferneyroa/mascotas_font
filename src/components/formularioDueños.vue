<template>
    <div class="formDueños">


<fieldset>
    <legend>Formulario Registro Dueños</legend>
        <form action="">

            <label for="idDueño">id de dueños</label><br>
            <input type="text" name="idDueño" id="idDueño" v-model="dueño.idDueño"><br>

            <label for="nombre">nombre</label><br>
            <input type="text" name="nombre" id="nombre" v-model="dueño.nombre"><br>

            <label for="apellidos">apellidos</label><br>
            <input type="text" name="apellidos" id="apellidos" v-model="dueño.apellidos"><br>

            <label for="direccion">direccion</label><br>
            <input type="text" name="direccion" id="direccion" v-model="dueño.direccion"><br>

            <label for="telefono">telefono</label><br>
            <input type="text" name="telefono" id="telefono" v-model="dueño.telefono" ><br><br>

            <button type="submit" v-on:click="guardar()">Guardar</button>
            <button type="submit" v-on:click="eliminar(dueño.idDueño)">Eliminar</button>
        </form>
</fieldset>
    </div>


</template>

<script>
import axios from 'axios'

export default {
  name:'formularioDueños',
data:function (){
return{
dueño: {
idDueño:"",
nombre:"",
apellidos: "",
direccion:"",
telefono:""
}
}
},
methods:{
guardar(){

axios.post('http://localhost:8080/api/dueños',this.dueño)
.then(data=>{

console.log(data);

})

},eliminar(id){

    
    axios.delete('http://localhost:8080/api/dueños/'+id)
    .then(data=>{

console.log(data);

})
//location.reload()  
}
}
}

</script>


<style scoped>

.formDueños{

text-align: center;
padding: 5%;
font-family : inherit;

}



</style>