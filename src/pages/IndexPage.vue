<template>
  <q-page class="flex flex-center">
    <div class="panel">
      <Panel/>
    </div>
  </q-page>
</template>

<script setup>
  import Panel from '../components/Panel.vue'
</script>
<style scoped>
  .panel{
    width: 50%;
    height: 60vh;
    background-color: rgba(44, 103, 111, 0.177);

    box-shadow: 2px 2px 2px rgb(188, 188, 188), 3px 3px 2px grey,
    4px 4px 4px rgb(255, 255, 255);
  }


</style>
