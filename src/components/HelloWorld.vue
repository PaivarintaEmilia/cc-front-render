<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})


</script>

<template>
  <div class="greetings">
    <h1 class="green">{}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>

  <div class="container">
    <div class="white-box">
      <p>Kirjoita tekstisi tähän: change</p>
      <input v-model="userInput" type="text" placeholder="Kirjoita tähän...">
      <button @click="submitText">Lähetä tekstisi</button>
    </div>
  </div>


</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}


.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.white-box {
  display: flex;
  flex-direction: column;
  justify-content: space-around; /* Tämä auttaa jakamaan sisällön tasaisesti */
  align-items: center; /* Keskitetään sisältö vaakasuunnassa */
  width: 300px;
  height: 200px;
  background-color: white;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  padding: 20px; /* Lisätään padding, jotta sisältö ei ole aivan laatikon reunoilla */
}

input {
  width: 100%; /* Täyttää vanhemman leveyden */
  padding: 10px; /* Lisätään padding, jotta teksti ei ole aivan input-kentän reunoilla */
  margin: 10px 0; /* Varmistetaan, että input-kentän ympärillä on tilaa */
  border: 1px solid #ccc; /* Määritellään kehys */
  border-radius: 5px; /* Pyöristetään input-kentän kulmat */
}

button {
  padding: 10px 20px; /* Määritellään painikkeen padding */
  border: none; /* Poistetaan kehys */
  background-color: #007bff; /* Määritellään taustaväri */
  color: white; /* Määritellään tekstin väri */
  border-radius: 5px; /* Pyöristetään painikkeen kulmat */
  cursor: pointer; /* Muuttaa kursorin osoittimen muotoon, kun se on painikkeen päällä */
}
</style>
