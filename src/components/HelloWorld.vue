<template>
    <div class="hello">

        <v-app-bar absolute color="#fcb69f" dark src="https://picsum.photos/1920/1080?random"
            scroll-target="#scrolling-techniques-2">
            <div class="hidden-md-and-up">
                <v-menu bottom right>
                    <template v-slot:activator="{ on }">
                        <v-btn dark icon v-on="on">
                            <v-icon>mdi-dots-vertical</v-icon>
                        </v-btn>
                    </template>

                    <v-list>
                        <v-list-item v-for="item in menu" :key="item.icon">

                            <v-list-item-title>{{ item.title }}</v-list-item-title>
                        </v-list-item>
                    </v-list>
                </v-menu>
            </div>


            <v-toolbar-title>Page title</v-toolbar-title>

            <v-spacer></v-spacer>

            <v-toolbar-items class="hidden-sm-and-down">
                <v-btn text v-for="item in menu" :key="item.icon">{{ item.title }}</v-btn>
            </v-toolbar-items>

            <v-btn icon>
                <v-icon>mdi-heart</v-icon>
            </v-btn>
        </v-app-bar>

        <v-content style="padding-top:200px">
            <v-container class="fill-height" fluid>
                <v-row align="center" justify="center">
                    <Card />
                    <Card />
                    <Card />
                </v-row>
                <v-row align="center" justify="center">
                    <Card />
                    <Card />
                    <Card />
                </v-row>
            </v-container>
        </v-content>
 
    </div>
</template>

<script>
  import Card from "@/components/Card.vue"
    export default {
        name: "HelloWorld",
        props: {
            msg: String
        },
        components:{ Card },
        data: () => {
            return {
                menu: [{
                        icon: 'home',
                        title: 'Home'
                    },
                    {
                        icon: 'info',
                        title: 'Sobre'
                    },
                    {
                        icon: 'warning',
                        title: 'Contato'
                    }
                ]
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>