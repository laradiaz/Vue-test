<template>
    <v-app>
        <v-content>
            <router-view/>
            <v-footer absolute class="font-weight-medium" color="blue-grey darken-2">
                <v-col class="text-center" cols="12">
                    Copyright 2020 - <a href="http://www.test.com">TestCompany</a>
                </v-col>
            </v-footer>
        </v-content>
    </v-app>
</template>

<script>


    export default {
        name: 'App',

        components: {},


        data: () => ({
            //
        }),
    };
</script>


<style lang="scss">
    #app {
        font-family: "Roboto", sans-serif;
        font-size: 18px;
        background-image: url("assets/login-bg.svg");
        background-size: cover;
        background-position: center right;
    }
</style>