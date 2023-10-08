<template>
  
  <main>
    <Canvas :color="colorChanger" />

    <form class="panel-form" action="">
      <h1>Welcome to {{ schoolName }}</h1>
      <p>Find as in {{ address }}</p>
      <p>Max number of children is {{ children }}</p>
      <label for="name">
        Name:
        <input type="text" name="name" id="name" v-model="schoolName">
      </label>

      <label for="color">
        Color:
        <input type="text" name="color" id="color" v-model="color">
      </label>

      <label for="address">
        Address:
        <input type="text" name="address" id="address" v-model="address">
      </label>

      <label for="children">
        Max number of children:
        <input type="text" name="children" id="children" v-model="children">
      </label>
    </form>

    


  </main>


</template>

<script setup>

const schoolName = ref('');
const color = ref('');
const address = ref('');
const children = ref('');


// Watch for changes in color and update color ref accordingly
watch(color, (newValue) => {
  color.value = newValue;
});

// Watch for changes in color and update color ref accordingly
watch(address, (newValue) => {
  address.value = newValue;
});


</script>

<style scoped>

main{
  width: 100vw;
  height: 100vh;
  display: flex;
  margin: 0 auto;
  align-items: center;
  justify-content: flex-start;

}

h1{
  color: black;
}

.panel-form{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  border: 2px solid red;
  width: 20%;
  height: 60%;
  margin: 0 auto 0 5rem;
}

</style>
