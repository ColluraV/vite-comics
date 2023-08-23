<script>

export default {
  data() {
    return {
      navLinks: [
        { name: "CHARACTERS" },
        { name: "COMICS"},
        { name: "MOVIES"},
        { name: "TV" },
        { name: "GAMES" },
        { name: "COLLECTABLES" },
        { name: "VIDEOS" },
        { name: "FANS" },
        { name: "NEWS" },
        { name: "SHOP" },
      ],
    };
  },
};

</script>

<template>
  <header class="">

    <div class="d-flex justify-content-around">
      
      <div class=" my-4">        <!-- //////logo////// -->
        <img src="../assets/dc-logo.png" alt="">
      </div>

      <div class="LinkContainer d-flex align-items-center justify-content-evenly">

        <div class="subbed d-flex" v-for="link in navLinks"> <!-- //////links top////// -->
          <a
            href="#"
            class="nav-link">
            {{ link.name }}
          </a>
        </div>

      </div>

    </div>

  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

header {


  .container{
    height: 100%;
    ul{
      margin-top: auto;
      margin-bottom: auto;
    }
  }

  img {
    width: 80px;
  }

  .nav-link {

    color: $colorText;
    font-weight:700;
   
  }


  .subbed{
    border-bottom: 3px solid transparent;
    margin-left: 1rem;

  }

  .subbed:hover { border-bottom:2px solid $color-primary;}
    
  

}

</style>
