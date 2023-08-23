<script>
    export default {

        props:{
            imgSrc:String,
            serie:{
                type: String,
                required: true,
            },
            tipologia:{
                type: String,
                required: true,
            },
            tipologia:{
                type: String,
                required: true,
            },
            prezzo: {type:Number},
                          

        }


    }


</script>

<template>

    <div class="card border-0 rounded-0 h-100"> 
        <img class=" relative" :src="imgSrc" alt="" /><!-- //////immagine////// -->

        <div class="card-body text-white bg-dark"> <!-- //////nome////// -->
        {{ serie }}
        </div>

        <div class="overlay"> <!-- //////info in hover////// -->
            <div class="absolute top hidden">Tipologia: <br>{{ tipologia }}</div>
            <div class="absolute bottom hidden">Prezzo: {{ prezzo }}</div>
        </div>

    </div>
        

        

</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

    .darkBanner{
        background-color: $colorDark;
    }
    
    .hidden{
        display: none;
    }
    .absolute{
        position: absolute;
        color: white;
        padding: 1rem 0;
        width: 100%;
    }
    .relative{
        position: relative;
    }
    .top{
        top: 5%;
        background-color: rgba(0, 0, 0, 0.652);
    }

    .bottom{
        bottom: 35%;
        right: 0;
        background-color: rgba(0, 0, 0, 0.652);
    }
    .card:hover .hidden{
        display: block;
    }

</style>