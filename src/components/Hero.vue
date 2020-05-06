<template>
    <v-container class="section pa-0" fluid>
        <v-row no-gutters justify="center">
            <v-col cols="12" md="10" lg="7" xl="7"
                   class="hero">

                <v-row no-gutters>
                    <v-col  cols="2">

                    </v-col>
                    <v-col cols="4" lg="5">

                            <v-card v-for="item in heroinf" :key="item.index"
                                    flat
                                    class="heroinfo">
                                <v-card-title class="primary--text title">
                                    {{item.title}}
                                </v-card-title>
                                <v-card-subtitle class="black--text">
                                    {{item.subtitle}}
                                </v-card-subtitle>
                            </v-card>

                    </v-col>
                </v-row>

            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "Hero",

        computed: {

            heroinf() {
                return [
                    {title: "Бизнесвумен",  subtitle: "Основала агентство контент-маркетинга Malkki Media, организатор мероприятий."},
                    {title: "Писатель",     subtitle: "Автор книг о жизни и воспитании детей в Финляндии."},
                    {title: "Блогер",       subtitle: "В Instagram блог о бизнесе и текстах."}
                ]
            }
        }
    }

</script>

<style scoped>
    @font-face {
        font-family: Cyrvetica;
        src: url(fonts/cyrvetica-extra-outline.ttf);
    }

    .section{
        height: calc(100vh - 84px);
        max-height: 816px;
        background: white url("../../src/assets/bghero.png") bottom right no-repeat;

    }

    .hero{
        height: calc(100vh - 84px);
        max-height: 816px;
        background: transparent url("../../src/assets/hero.png") top 63px right no-repeat;
        background-size: contain;
    }

    .heroinfo{
        background-color: rgba(255,255,255, 0);
    }

    .title{
        font-family: Cyrvetica !important;
        font-size: 48px;
        text-transform: uppercase;
    }

</style>