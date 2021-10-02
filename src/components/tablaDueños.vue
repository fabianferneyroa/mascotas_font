<template>
    <div class="clas">
  

        <fieldset>
            <legend>Tabla de Dueños</legend>
<table>
  <tr>
    <th>id</th>
    <th>nombre</th>
    <th>apellidos</th>
    <th>direccion</th>
    <th>telefono</th>
  </tr>
  <tr v-for="dueño in dueños" :key="dueño.idDueño">
    <td>{{dueño.idDueño}}</td>
    <td>{{dueño.nombre}}</td>
    <td>{{dueño.apellidos}}</td>
    <td>{{dueño.direccion}}</td>
    <td>{{dueño.telefono}}</td>
  </tr>
  
</table>
        </fieldset>

        <router-view/>
    </div>

</template>

<script>
import axios from 'axios'
export default{
name:'tablaDueños',
data(){
  return{
     dueños:[]
  }
},
mounted(){
  let vue=this;
  axios.get('http://localhost:8080/api/dueños/listar')
  .then( response =>{

    vue.dueños=response.data;
  })
},methods:{


  
}

}

</script>

<style scoped>

.tablaDueños{
padding: 5%;
text-align: center;

}
table{
    
    border: 1px solid #000;
    margin: auto;
    padding: 1 px;
}
th{

border: 1px solid #000;

}
tr,td{
    
    width: 20%;
   text-align: left;
   vertical-align:top;
   border: 1px solid #000;
}
</style>