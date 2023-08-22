<script>
    export default {
  data() {
    return {
      navLinks: [
        { name: "DIGITAL COMICS", img: "buy-comics-digital-comics.png" },
        { name: "DC MERCHANDISE", img: "buy-comics-merchandise.png" },
        { name: "SUBSCRIPTION", img: "buy-comics-subscriptions.png" },
        { name: "COMIC SHOP LOCATOR", img: "buy-comics-shop-locator.png" },
        { name: "DC POWER VISA", img: "buy-dc-power-visa.svg" },
      ],
    };
  },
};
</script>

<template>

    <main>

        <div class="raw zonaMid darkBanner">
            <div class="container">
                <h2> Content goes here </h2>
            </div>
        </div>

        <div class="raw zonaMid blueBanner">

            <div class="container">

                <ul class="nav nav-pills">
                    <li class="nav-item" v-for="link in navLinks">
                     <a
                         href="#"
                         class="nav-link">
                         <img v-bind:src="`/src/assets/${link.img}`" class="bannerImg" alt="" />
                         {{ link.name }}

                     </a>
                    </li>
                </ul>
    
            </div>


        

        </div>
    </main>
    
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

    .zonaMid{
        min-height: 150px;
    }

    .darkBanner{
        background-color: $colorDark;
    }
    .blueBanner{
        background-color: $color-primary;
        color: white;
    }

    h2{
        color: white;
    }
    .bannerImg{
        width: 80px;
    }
</style>