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
            <div class="col-6 d-flex flex-column flex-wrap py-4">

                <div class="bottomLinks ">   <!-- //////links array in v-for////// -->
                    <h5> DC COMICS </h5> 
                    
                        <div class="" v-for="link in DcComicsLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </div>
                    
                </div>


                <div class="bottomLinks">   <!-- //////links array in v-for////// -->
                    <h5> SHOPS </h5>

                    
                        <div class="" v-for="link in ShopLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </div>
                    
                </div>

                <div class="bottomLinks">   <!-- //////links array in v-for////// -->
                    <h5> DC </h5>

                    
                        <div class="" v-for="link in DCLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </div>
                    
                </div>
                <div class="bottomLinks">
                    <h5> SITES </h5>

                    
                        <div class="" v-for="link in SitesLinks">
                        <a 
                          href="#"
                          class="">
                          {{ link.name }}
                        </a>
                        </div>
                    
                </div>
            </div>
            <div id="cutted" class="col-6"></div><!-- ////// dc logo////// -->
                

        </div>

        <div class="contacts align-content-middle">
            <div class="container d-flex justify-content-between">
                <button type="button" class="btn btn-outline-primary">SIGN-UP NOW</button>
                <div class="socials">                       <!-- //////socials////// -->
                    FOLLOW US
                    <img src="../assets/footer-facebook.png" alt="">
                    <img src="../assets/footer-periscope.png" alt="">
                    <img src="../assets/footer-pinterest.png" alt="">
                    <img src="../assets/footer-twitter.png" alt="">
                    <img src="../assets/footer-youtube.png" alt="">
                </div>
            </div>
        </div>

    </footer>

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

    .bottomLinks{
       max-width: 250px;
    }


    div a{
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
        height: 350px;
    }

    .contacts{
        background-color: #303030;
        height: 200px;
        >.container{
            height: 100%;
            margin-top: auto;
            margin-bottom: auto;
        }
    }
    .btn-outline-primary{
        border-radius: 0;
        color: white;
        font-size: 1.1rem;
        height: 80px;
        margin-top: auto;
        margin-bottom: auto;
    }

    .socials{
        color:$color-primary;
        font-size: 1.1rem;
        font-weight: 600;
        margin-top: auto;
        margin-bottom: auto;
        > img{
            margin: 0 10px;

        }
    }

    #cutted{
        background-image: url(../assets/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: center;
    }
</style>
