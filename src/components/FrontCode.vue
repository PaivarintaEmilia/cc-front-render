<script setup>



</script>

<template>

  <div class="container">
    <div class="white-box">
      <p>Submit a sentence for the sentiment analysis here</p>
      <input v-model="userInput" type="text" placeholder="Write your sentence here...">
      <button @click="submitText">SUBMIT</button>
    </div>
  </div>


</template>

<style scoped>

p {
  font-size: 22px;
  font-weight: 500;
  font-family: monospace;
  color: rgb(39, 39, 39);
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
  width: 800px;
  height: 200px;
  background-color: rgb(214, 234, 251);
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(81, 98, 249, 0.325);
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


@media (min-width: 1024px) {
  p {
    text-align: center;
    color: rgb(66, 66, 66);
  }

  .white-box {
    width: 900px;
  }
}

@media (max-width: 768px) {
  p {
    text-align: center;
    color: rgb(44, 44, 44);
  }

  .white-box {
    width: 90%;
    height: 300px;
  }
}

@media (max-width: 480px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }

  .white-box {
    width: 90%;
    padding-top: 50px;
    padding-bottom: 50px;
  }

  p {
    font-size: 1.1em;
    text-align:  center;
    color: #007bff;
  }
}



</style>
