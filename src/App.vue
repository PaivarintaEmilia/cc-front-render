<script setup>
  import FrontCode from './components/FrontCode.vue'
</script>

<template>
<header>

</header>

<main>
  <div class="wrapper">
    <FrontCode />
  </div>
  
</main>
</template>

<style scoped>
header {
  line-height: 1.5;
}


@media (min-width: 1024px) {
    header {
      display: flex;
      place-items: center;
      /*padding-right: calc(var(--section-gap) / 2);*/
    }

    main {
      display: flex;
      place-items: center;
      /*padding-right: calc(var(--section-gap) / 2);*/
    }


    header .wrapper {
      display: flex;
      place-items: flex-start;
      flex-wrap: wrap;
    }
  }


</style>
