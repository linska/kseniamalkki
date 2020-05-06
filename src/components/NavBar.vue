<template>
    <v-container fluid class="py-5 px-0">
        <v-row no-gutters justify="center">
            <v-col  cols="12" sm="12" md="10" lg="7" xl="7">
                <v-row no-gutters align="center">
                    <v-col cols="2" md="1" lg="1" xl="1">
                        <v-img src="../../src/assets/logo.png"
                               contain
                               width="69"/>
                    </v-col>
                    <v-col cols="10" md="11" lg="11" xl="11">
                        <v-row no-gutters justify="end" class="hidden-sm-and-down">
                            <v-btn class="button primary--text text-none"
                                   v-for="item in barbtn" :key="item.title"
                                   :to=item.target
                                   depressed>
                                {{ item.title}}
                            </v-btn>
                        </v-row>
                        <v-row no-gutters justify="end" class="hidden-md-and-up">

                            <v-menu offset-y>
                                <template v-slot:activator="{on}">
                                    <v-btn class="button primary--text text-none"
                                           depressed
                                           v-on="on">

                                        <v-img src="../../src/components/icons/menu.svg"></v-img>
                                    </v-btn>
                                </template>
                                <v-card v-for="item in barbtn" :key="item.title"
                                        flat>
                                    <v-btn class="button buttonnav primary--text text-none"
                                           :to=item.target
                                           depressed>
                                        {{ item.title}}
                                    </v-btn>
                                </v-card>
                            </v-menu>
                        </v-row>
                    </v-col>
                </v-row>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "NavBar",

        computed: {
            barbtn() {
                return [
                    {title: 'Обо мне',       icon:"", target:"",},
                    {title: 'Консультации',  icon:"", target:"",},
                    {title: 'Мои проекты',   icon:"", target:"",},
                    {title: 'Книги',         icon:"", target:"",},
                    {title: 'Халява, плиз!', icon:"", target:"",},
                    {title: 'Контакты',      icon:"", target:"",}
                ]
            }
        }
    }
</script>

<style scoped>
    .button{
        font-family: 'Roboto', sans-serif;
        font-weight: normal;
        letter-spacing: normal;
        font-size: 18px;
        background-color: transparent !important;
    }
    .buttonnav{
        width: 100%;
    }
</style>