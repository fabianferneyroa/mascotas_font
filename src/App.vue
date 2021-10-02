<template>
  <div id="app">
           <div><img src="./assets/head.png" alt=""></div>


      <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/mascotas">Mascotas</router-link> |
      <router-link to="/dueños">Dueños</router-link>

    </div>

    <div class="contenedor">
 <router-view/>
</div>
    <footer>pie pagina</footer>
  </div>
  
</template>

<style>

.contenedor{

  width: 100%;
}



#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  border: 1px solid black;
  
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: cadetblue;
}
</style>
