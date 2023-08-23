<script>
import TheHeader from "./components/TheHeader.vue";
import TheMid from "./components/TheMid.vue";
import TheFooter from "./components/TheFooter.vue";
import comicsCards from "./components/comicsCards.vue";
import dcComicsList from "./db/dc-comics.json";


export default {
  components: {
    TheHeader,
    comicsCards,
    TheMid,
    TheFooter
  },
  data() {
    return {
      dcComicsList,
    };
  },
};
</script>

<template>
<TheHeader/>
<main>

  <div class="container text-center">
      <h3 class="text-secondary">Lista Prodotti</h3> 
  <comicsCards/>
  <TheMid/>
</div>
</main>

<TheFooter/>

</template>

<style scoped>



</style>
