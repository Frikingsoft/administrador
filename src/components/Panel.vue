<template>
  <div class="flex wrap justify-evenly q-mt-md">
    <template v-for="(opcion, index) in opciones" :key="index">
      <div class="opciones row">
        <q-icon :name="`${opcion.icono}`" size="35px" color="white" class="boton q-mb-md col-12 flex flex-center"/>
        <span class="col-12 flex justify-center">{{opcion.nombre}}</span>

      </div>
    </template>
  </div>

</template>
<script setup>
  import { ref } from "vue";
  const opciones = ref([
    {nombre:"Respaldo",icono:"fas fa-box-archive",url:""},
    {nombre:"Lenguaje",icono:"fas fa-language",url:""},
    {nombre:"Logs",icono:"fas fa-circle-exclamation",url:""},
    {nombre:"Actualizacion",icono:"fas fa-file-arrow-down",url:""},
    {nombre:"Usuarios",icono:"fas fa-users",url:""}
  ])
</script>
<style scoped>
  .opciones{
    width: 150px;
    height: 150px;
    border-radius:50%;
    box-shadow: 0 0 3px rgba(14, 81, 163, 0.471),1px 1px 5px rgba(14, 81, 163, 0.471);
    color: white;
    border: 2px solid rgba(14, 81, 163, 0.471);
    font-size: 1.3em;
  }
  .opciones:hover::after {
    content: " ";
    position: absolute;
    width: 150px;
    height: 150px;
    border-radius: 50%;
    animation: 1s animar infinite linear;
    background-image: conic-gradient(rgba(15, 69, 136, 0.343) 5deg, rgba(14, 81, 163, 0.471) 10deg, transparent 360deg);

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
