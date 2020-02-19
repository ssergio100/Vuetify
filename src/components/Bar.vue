<template>
    <div class="bar">

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
 
    </div>
</template>

<script>
    export default {

       
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
