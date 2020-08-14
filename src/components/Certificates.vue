<template>
    <div color="grey">
        <v-container>
            <v-row justify="center" class="headline">
                Certificates relevant to Web Development
            </v-row>
        </v-container>
        <v-container>
           <v-row>
               <v-col cols="12" sm="6" v-for="certificate in certificates" :key="certificate.id">
             <v-hover v-slot:default="{ hover }">
                 <v-card class="mx-auto" color="grey lighten-4" max-width="600">
                     <v-img :aspect-ratio="16/9" :src="certificate.image">
                         <v-expand-transition>
                            <div
                             v-if="hover"
                             class="d-flex transition-fast-in-fast-out black darken-2 v-card--reveal display-6 white--text"
                             style="height: 100%;"
                           >
                           {{certificate.desc}}
                             </div>
                          </v-expand-transition>
                     </v-img>
                     <v-card-text class="pt-6" style="position: relative;" >
                     <div class="black--text title mb-2">{{certificate.head}}</div>
                     </v-card-text>
                 </v-card>
              </v-hover>
               </v-col>
           </v-row>
        </v-container>
    </div>
</template>
<script>
export default {
    name:"Certificates",
    data(){
        return{
            certificates:[
                {
                    id:1,
                    head:"Front-End Web Development With React",
                    image:require('../assets/React-1.jpg'),
                    desc:"JavaScript has revolutionised the world of Web Development.With the emergence of various frameworks and libraries, web development and designing has become far easier.Through this course, I learnt React-the most widely used JavaScript framework and Redux. I built the website for a hotel using React in this course."
                },
                {
                    id:2,
                    head:"Front-End Web UI Frameworks:Bootstrap4",
                    image:require('../assets/UI-1.jpg'),
                    desc:"In this course, I learnt the usage of Bootstrap- a CSS framework and also built the website of a hotel which included its menu oage, hotel reservation page and contacts page."
                },
                {
                    id:3,
                    head:"The complete 2020 Web Development Bootcamp",
                    image:require('../assets/0001.jpg'),
                    desc:"This course introduced me to the world of web development. I learnt about  frontend development- HTML,CSS,Bootstrap,JavaScript, React and backend development-Express, NodeJS, MongoDB, Mongoose,RESTful APIs.I made several projects in this course."
                }
            ]
        }
    }
}
</script>
<style scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
</style>