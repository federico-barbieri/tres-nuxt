<template>
    <div class="wrapper">
  
   <TresCanvas width="100%" height="100%" clear-color="transparent" preset="realistic">
        <OrbitControls />
        <TresMesh :scale="[2, 0.5, 1]">
            <TresBoxGeometry />
            <TresMeshNormalMaterial />
        </TresMesh>
  </TresCanvas>
  </div>
  
  
  
  </template>
  
  <script setup>


  
  </script>
  
  <style scoped>
  
  .wrapper{
    width: 100%;
    height: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0;
  }
  
  </style>