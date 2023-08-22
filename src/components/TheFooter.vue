<script>
 export default {
  data() {
    return {
      DcComicsLinks: [
        { name: "Characters"},
        { name: "Comics" },
        { name: "Movies"},
        { name: "Tv"},
        { name: "Games"},
        { name: "Videos"},
        { name: "News"},
        ],
      ShopLinks:[
        { name: "Shop Dc"},
        { name: "Shop Collectables" },
        ],
      DCLinks:[
        { name: "Terms Of Use"},
        { name: "Privacy Policy(New)" },
        { name: "AdChoice"},
        { name: "Advertising"},
        { name: "Jobs"},
        { name: "Subscriptions"},
        { name: "Talent Workshops"},
        { name: "CPSC Certificates"},
        { name: "Ratings"},
        { name: "Shop Help"},
        { name: "Contact Us"},
        ],
      SitesLinks:[
        { name: "DC"},
        { name: "Mad Magazine"},
        { name: "DC Kids"},
        { name: "DC Universe"},
        { name: "DC Power Visa"},
        ],
    };
  },
};

</script>

<template>
    <footer>
        <div class="raw bottom d-flex">
            <div class="container d-flex flex-column flex-wrap py-5">

                <div class="bottomLinks ">
                    <H5> DC COMICS </H5>
                    <ul class="">
                        <li class="" v-for="link in DcComicsLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </li>
                    </ul>
                </div>


                <div class="bottomLinks">
                    <H5> SHOPS </H5>

                    <ul class="">
                        <li class="" v-for="link in ShopLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </li>
                    </ul>
                </div>

                <div class="bottomLinks">
                    <H5> DC </H5>

                    <ul class="">
                        <li class="" v-for="link in DCLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </li>
                    </ul>
                </div>
                <div class="bottomLinks">
                    <H5> SITES </H5>

                    <ul class="">
                        <li class="" v-for="link in SitesLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </li>
                    </ul>
                </div>
            </div>


        </div>
            <div class="contacts raw">
                <div class="container">
                    <div class="login">gfdgfdgdf</div>
                    <div class="socials">gfdgdfgd</div>
                </div>
            </div>

    </footer>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

    .bottomLinks{
       max-width: 250px;
    }
    .bottomLinks li{
        list-style: none;
    }


    .bottomLinks li a{
        text-decoration: none;
        color: gray;
    }
    .bottom{
        background-image: url(../assets/footer-bg.jpg);
        background-size: cover;
    }

    h5{
        color: white;
    }

    .raw.bottom{
        height: 500px;
    }
</style>
