<template>
    <div>
        <v-container grid-list-xs>
            <v-row>
                <v-container>
                <div class="black--text display-2">Skills</div>
                <v-timeline align-top :dense="$vuetify.breakpoint.smAndDown">
                   <v-timeline-item v-for="skill in skills" :key="skill.id" :color="skill.color" fill-dot>
                     <v-card :color="skill.color" dark>
                         <v-card-title class="title">{{skill.name}}</v-card-title>
                          <v-card-text class="white text--primary">
                           <v-rating v-model="skill.rating" background-color="orange lighten-3" color="orange"></v-rating>
                          </v-card-text>
                     </v-card>
                   </v-timeline-item>
                </v-timeline>
                      
                </v-container>
            </v-row>
        </v-container>
        <v-divider></v-divider>
    </div>
</template>
<script>
export default {
    name:"Skills",
    data(){
        return{
            skills:[
                {
                    id:1,
                    name:"HTML,CSS,Bootstrap",
                    color:"red lighten-1",
                    rating:5

                },
                {
                    id:2,
                    name:"JavaScript",
                    color:"purple darken",
                    rating:5
                },
                {
                    id:3,
                    name:"Vue",
                    color:"rgb(66, 135, 245)",
                    rating:4
                },
                {
                    id:4,
                    name:"ReactJS",
                    color:"indigo",
                    rating:3
                },
                {
                    id:5,
                    name:"Express",
                    color:"rgb(247, 121, 214)",
                    rating:4
                },
                {
                    id:6,
                    name:"NodeJS",
                    color:"rgb(255,122,12)",
                    rating:4

                },
                {
                    id:7,
                    name:"Mongoose",
                    color:"rgb(110, 194, 129)",
                    rating:4

                },
                {
                    id:8,
                    name:"RESTful APIs",
                    color:"rgb(255, 84, 84)",
                    rating:3
                },
                {
                    id:9,
                    name:"C++",
                    color:"rgb(84, 255, 189)",
                    rating:5
                }
            ]
        }
    }
}
</script>
<style scoped>
</style>