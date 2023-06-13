<template>
   <div class="menu">
    <nav>
       <template v-for="(boton,index) in botones" :key="index">
          <q-icon :name="`${boton.nombre}`" size="35px" color="white" class="boton q-mb-md"/>
       </template>

    </nav>
   </div>
</template>
<script setup>
  import { ref } from "vue"
  const botones = ref([
    {nombre:"fas fa-gear", ruta:"/"},
    {nombre:"fas fa-server", ruta:"/"},
    {nombre:"fas fa-screwdriver-wrench", ruta:"/"},
    {nombre:"fas fa-network-wired", ruta:"/"},
    {nombre:"fas fa-database", ruta:"/"},
    {nombre:"fas fa-share-nodes", ruta:"/"}
  ])
</script>
<style scoped>
  .menu{
    position: fixed;
    top: 0;
    width: 60px;
    height: 100vh;
    z-index: 1;

  }
  .menu nav{
    width: 100%;
    height: 100%;
    background-color: rgba(44, 103, 111, 0.177);
     box-shadow: 2px 2px 2px rgb(188, 188, 188), 3px 3px 2px grey,
        4px 4px 4px black;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .boton:hover::after{
    position: fixed;
    content: " ";
    width: 50px;
    height: 50px;
    border-radius: 50%;
    box-shadow: 0 0 3px white;
    animation: 1s animar infinite linear;
    background-image: conic-gradient(rgba(255, 255, 255, 0.586) 5deg, rgba(222, 218, 218, 0.273) 10deg, transparent 210deg);
  }
  .boton:hover{

  }
  @keyframes animar{
    from {
      transform: rotate(0);
    }
    to{
      transform: rotate(360deg);
    }
  }
</style>
