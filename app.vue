<template>
  
  <main>
    <Canvas :color="colorChanger" />

    <form class="panel-form" action="">
      <h1>Welcome to {{ schoolName }}</h1>
      <label for="name">
        Name:
        <input type="text" name="name" id="name" v-model="schoolName">


      </label>

      <label for="color">
        Color:
        <input type="text" name="color" id="color" v-model="inputValue">

      </label>
    </form>

    


  </main>


</template>

<script setup>

const schoolName = ref('');


const inputValue = ref('');
const colorChanger = ref('');

// Watch for changes in inputValue and update colorChanger accordingly
watch(inputValue, (newValue) => {
  colorChanger.value = newValue;
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
