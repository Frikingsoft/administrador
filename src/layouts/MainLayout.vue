<template>
  <q-layout view="lHh Lpr lFf">
    <Menu/>
    <q-page-container>
       <q-img
          src="icono.png"
          :ratio="16/9"
         class="icono"/>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
  import Menu from './Menu.vue'

</script>
<style scoped>
  .icono{
    position: fixed;
    margin-left: 70px;
    width: 256px;
    height: 256px;
  }
</style>
