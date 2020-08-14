<template>
<div>
    <v-app-bar color="rgb(145, 0, 63)" dark prominent class="px-0 mx-0"  height="75">
        <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
        
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute temporary color="pink lighten-4">
        <v-list nav dense v-for="item in items" :key="item.id">
            <v-list-item router :to="{name:item.route}">
                <v-list-item-content>
                    <v-list-item-title><h3>{{item.name}}</h3></v-list-item-title>
                </v-list-item-content>                
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</div>
</template>
<script>
export default {
    name:"Header",
    data(){
        return{
            drawer:true,
            items:[
                {
                    id:1,
                    name:"Home Page",
                    route:"Home"
                },
                {
                    id:2,
                    name:"Projects",
                    route:"Projects"

                },
              
            ]
        }
    }
}
</script>
<style scoped>
</style>