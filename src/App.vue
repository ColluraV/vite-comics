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

  <div class="row zonaMid darkBanner py-5">
    <div class="container text-center">
      <h3 class="text-secondary">Lista Fumetti</h3> 

      <div id="cards_container" class="row row-cols-6 gy-3 my-3">

        <!--////////////// cards in ciclo for //////////////// -->
        <div class="col" 
        v-for="(card,i) in dcComicsList"
        :KEY="`card_${i}`"
        >
          
            <comicsCards 
                :img-src="card.thumb"
                :serie="card.series" 
                :prezzo="card.price"
                :tipologia="card.type"  
              />
        
        </div>
      </div>

      <TheMid/>

    </div>
  
  
  </div>
  
</main>

<TheFooter/>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

    .darkBanner{
        background-color: $colorDark;
    }
    #cards_container{
      max-width: 1100px;
      margin: auto;
    }
</style>
