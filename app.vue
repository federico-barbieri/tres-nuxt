<template>
  
  <main>
    <section class="left-side">

    
    <div class="daycare-info">
      <h1>Welcome to {{ schoolName }}</h1>
      <p>Find as in {{ address }}</p>
      <p>Max number of children is {{ children }}</p>
    </div>
    <Canvas class="canvas" />

  </section>

  <section class="right-side">

    <form class="panel-form" action="">

<label for="name">
  Name:
  <input type="text" name="name" id="name" v-model="schoolName">
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



  </section>    


  </main>


</template>

<script setup>

const schoolName = ref('');
const address = ref('');
const children = ref('');


// Watch for changes in color and update color ref accordingly
watch(address, (newValue) => {
  address.value = newValue;
});


</script>

<style scoped>

/* main */

main{
  width: 80vw;
  height: 90vh;
  display: flex;
  flex-direction: row;
  margin: auto;
  align-items: center;
  justify-content: space-around;
  border: 2px solid black;
  overflow: hidden;

}

/* left side */

.left-side{
width: 70%;
height: 100%;
display: flex;
flex-direction: column;
align-items: center;
justify-content: space-around;
border: 2px solid green;

}

.daycare-info{
  width: 90%;
  height: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  background-color: magenta;
  border-radius: 30px;
  color: white;
  padding: 1rem;
}


/* right side */

.right-side{
width: 30%;
height: 100%;
display: flex;
flex-direction: column;
align-items: center;
justify-content: space-around;
border: 2px solid green;

}

.panel-form{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  border: 2px solid red;
  max-width: 100%;
  height: 100%;
  margin: 0 auto;
}

</style>
