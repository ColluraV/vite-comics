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
        ]
    };
  },
};
</script>

<template>


        <div class="raw zonaMid blueBanner">

            <div class="container d-flex justify-content-center py-5">

                <ul class="nav nav-pills ">
                    <li class="nav-item my-auto" v-for="link in navLinks">
                     <a
                         href="#"
                         class="nav-link text-white">
                         <img v-bind:src="`/src/assets/${link.img}`" class="bannerImg" alt="" />
                         {{ link.name }}

                     </a>
                    </li>
                </ul>
            </div>
        </div>
        

   
    
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

    .zonaMid{
        min-height: 150px;
    }

    .blueBanner{
        background-color: $color-primary;
        color: white;
    }

    .bannerImg{
        max-height: 70px;
        width: 50px;
    }


</style>