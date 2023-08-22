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

    <div class="container d-flex justify-content-between ">

      <div>        <!-- //////logo////// -->
        <img src="../assets/dc-logo.png" alt="">
      </div>

      <div>
        <ul class="nav ">
      <li class="nav-item" v-for="link in navLinks">
        <a
          href="#"
          class="nav-link">
          {{ link.name }}
        </a>
      </li>
    </ul>
      </div>

    </div>

  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

header {
  height:150px;

  img {
    width: 80px;
  }

  .nav-link {

    color: $colorText;
    font-weight:700;
   
  }

  li{
    height: 100%;
  }
}

</style>
