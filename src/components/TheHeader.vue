<script>

export default {
  data() {
    return {
      navLinks: [
        { name: "CHARACTERS", path: "/" },
        { name: "COMICS", path: "/products" },
        { name: "MOVIES", path: "/contacts" },
        { name: "TV", path: "/about" },
        { name: "GAMES", path: "/about" },
        { name: "COLLECTABLES", path: "/about" },
        { name: "VIDEOS", path: "/about" },
        { name: "FANS", path: "/about" },
        { name: "NEWS", path: "/about" },
        { name: "SHOP", path: "/about" },
      ],
    };
  },
};

</script>

<template>
  <header>

    <div class="container d-flex justify-content-between ">

      <div>        <!-- //////logo////// -->
        <img src="../assets/dc-logo.png" alt="">
      </div>

      <div>
        <ul class="nav ">
      <li class="nav-item" v-for="link in navLinks">
        <a
          href="#"
          class="nav-link"
          :class="{ active: link.name === 'Servizi' }"
        >
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
</style>
