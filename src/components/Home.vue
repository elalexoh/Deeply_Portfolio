<template>
    <div class="Home">
        <article class="hero bg-img" :style="{ backgroundImage: `url('${img}')` }">
            <section class="content container-fluid h-100">
                <div class="row h-50 w-100 mx-auto">
                    <!-- Introuction Content -->
                    <div class="col d-flex align-items-start justify-content-end flex-column">
                        <vue-typed-js 
                            :typeSpeed="100"
                            :backSpeed="50"
                            :strings="[
                                'Front-End', 
                                'Back-End',
                                'Fred_dev'
                            ]" 
                            :cursorChar="'_'"
                            class=""
                        >
                            <h1 class="typing"></h1>
                        </vue-typed-js>
                        <div class="introduction">
                            <p>
                                Lorem ipsum dolor sit 
                                amet consectetur adipisicing elit. Iure
                                eum rerum perferendis quia! 
                            </p>
                        </div>
                    </div>
                    <!-- Call to action -->
                    <div class="col d-flex align-items-end justify-content-end">
                        <a name="" id="" class="btn btn-primary " href="#" role="button">eat me!</a>
                    </div>
                </div>
                <div class="row h-50 d-flex align-items-end">
                    <div class="col p-0">
                        <div class="portfolio">
                            <carousel 
                                :autoplay="true" 
                                :nav="false"
                                @changed="changed"
                                :items="3"
                                :dots="false"
                                :loop="true"
                                >
                                <div class="item bg-img" style="background-image:url('https://placeimg.com/200/200/any?1');"></div>
                                <div class="item bg-img" style="background-image:url('https://placeimg.com/200/200/any?2');"></div>
                                <div class="item bg-img" style="background-image:url('https://placeimg.com/200/200/any?3');"></div>
                                <div class="item bg-img" style="background-image:url('https://placeimg.com/200/200/any?4');"></div>
                            </carousel>
                            <div class="box-proyect"></div>
                        </div>
                    </div>
                </div>
            </section>
        </article>
        <article class="animation d-flex justify-content-center align-items-center">
            <section class="animation-zone h-50 w-100 d-flex align-items-center justify-content-center">
                <h2 class="text-center">animation</h2>
            </section>
        </article>
    </div>
</template>
<script>
    // vue-owl-carousel solo se puede usar en el componente donde se va a declarar el template
    import carousel from 'vue-owl-carousel' 
    export default {
    name: 'Home',
    data () {
        return {
        msg: 'Hello there',
        img: 'https://via.placeholder.com/1366x800',
        }
    },
    components: { carousel },
    methods: {
        changed() {
            // console.log('hey listen');
        }
    }
}
</script>

<style lang="scss">
    @import "../styles/partials/_mixins.scss";
    .typed-cursor {
        font-size: 2.5rem;
    }
    .hero {
        height: 75vh;
    }
    .animation {
        height: 45vh;
        @include responsive(tablet){
            background-color: #bada55;
        }
    }
    .portfolio {
        $height_porfolio : 75vh;
        $mt_porfolio: 2vh;
        .item {
            height: ($height_porfolio / 2) - $mt_porfolio;
            margin-top: $mt_porfolio;
        }
    }
</style>