<template>
    <div>
        <header style="height: 320px" class="primary text-center white--text py-4">
            <v-container>
                <h1 class="display-1 pt-6">Compare Over 50 Life Insurance Quotes</h1>
                <h3>Affordable premiums from just £1.15 per week*</h3>
            </v-container>
        </header>
        <v-container>
            <theForm/>
        </v-container>
        <section class="pt-0">
            <v-container class="pt-16">
                <v-row justify="space-around">
                    <v-col cols="11" sm="9" md="8">
                        <div class="text-center">
                            <h2 class="text--primary display-1">Get a Life Insurance Quote in 3 Easy Steps</h2>
                            <span class="ml-auto mr-auto bigUnderline"></span>
                        </div>
                    </v-col>
                </v-row>
                <v-row class="mt-8 justify-space-around justify-sm-space-between">
                    <v-col class="text-center mb-4 mb-md-0" cols="10" sm="6" md="3">
                        <div class="px-3">
                            <img width="60" src="/icons/020-prototype.svg">
                            <h3 class="secondary--text" style="line-height: 26px">Free No-Obligation Quote</h3>
                        </div>
                    </v-col>
                    <v-col class="text-center pt-md-10 mb-4 mb-md-0" cols="10" sm="6" md="3">
                        <div class="px-3">
                            <img width="60" src="/icons/004-clock.svg">
                            <h3 class="secondary--text" style="line-height: 26px">Cover From £1.62 per week</h3>
                        </div>
                    </v-col>
                    <v-col class="text-center" cols="10" sm="6" md="3">
                        <div class="px-3">
                            <img width="60" src="/icons/006-manager.svg">
                            <h3 class="secondary--text" style="line-height: 26px">Protect loved ones</h3>
                        </div>
                    </v-col>
                </v-row>
            </v-container>
        </section>
    </div>
</template>
<script>
import theForm from '~/components/theForm.vue'
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
export default {
    data() {
        return {
            settings: {
                "dots": false,
                "centerPadding": "20px",
                "centerMode": true,
                "focusOnSelect": true,
                "infinite": true,
                "speed": 500,
                "slidesToShow": 3,
                "slidesToScroll": 3,
                "autoplay": true,
                "touchThreshold": 5,
                "responsive": [{
                    "breakpoint": 800,
                    "settings": {
                        "slidesToShow": 1,
                        "dots": true,
                    }
                }]
            },
        }
    },
    components: {
        theForm,
        VueSlickCarousel
    },
}
</script>
<style lang="scss">
.v-icon {
    color: orange;
}
section {
    padding: 3em 0;
}
.bigUnderline {
    width: 15%;
    background-color: #ff9800;
    display: block;
    height: 3px;
    margin-top: 20px;
    border-radius: 20px;
    max-width: 300px;
}
.v-expansion-panels {
    @media only screen and (min-width: 960px) {
        margin-top: 5em;
    }
}
.top-nudge {
    @media only screen and (min-width: 960px) {
        margin-top: 3em;
    }
}
.v-expansion-panel,
.v-expansion-panel::before {
    box-shadow: none !important;
}
.white-text {
    color: #fff;
}

.v-application {
    overflow-x: hidden;
}
</style>
