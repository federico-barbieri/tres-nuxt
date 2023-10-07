<template>
    <div class="wrapper">
  
   <TresCanvas width="100%" height="100%" :clear-color="color" preset="realistic">
        <OrbitControls />
        <TresMesh :scale="[2, 0.5, 1]">
            <TresBoxGeometry />
            <TresMeshNormalMaterial />
        </TresMesh>
  </TresCanvas>
  </div>
  
  
  
  </template>
  
  <script setup>

const props = defineProps({
  color: {
    type: String, // Replace PropType with the type of your prop (e.g., String, Number, Object, etc.)
    required: true, // Set to true if the prop is required
  },
});  
  
  </script>
  
  <style scoped>
  
  .wrapper{
    width: 40vw;
    height: 60vh;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 0 0 5rem;
  }
  
  </style>