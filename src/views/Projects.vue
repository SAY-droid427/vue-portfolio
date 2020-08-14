<template>
<div>
    <v-parallax src="../assets/image1.jpg" >
      <div v-ripple class="text-center">
           <h1 class="white--text">Projects</h1>   
           <h2 class="white--text">Assessment of knowledge and expertise is greater than earning a few certificates.</h2>        
       </div>
    </v-parallax>
 <v-container>
     <v-row justify="center">
         <v-col cols=12  v-for="project in projects" :key="project.id">
             <v-card class="mx-auto" max-width="1000">
                 <v-img :src="project.image" class="white--text" gradient="to bottom, rgba(0,0,0,0.5),rgba(0,0,0,0.9)" height="300px">
                 <v-card-title >
                     <h2>{{project.name}}</h2>
                 </v-card-title>
                 <v-card-text>
                     <h2>{{project.desc}}</h2>
                     <h2>{{project.techstack}}</h2>
                 </v-card-text> 
                 <v-card-actions>
                     <v-btn class="ml-auto" outlined color="white" :href="project.link">Check For Yourself</v-btn>
                 </v-card-actions>                             
                 </v-img>
             </v-card>
         </v-col>
     </v-row>
     </v-container>
 <Certificates />
</div>
</template>
<script>
import Certificates from "../components/Certificates"
export default {
    name:"Projects",
    components:{
     Certificates
    },
    data(){
        return{
            dialog:false,
            projects:[
                {
                    id:1,
                    name:"Weather App",
                    desc:"In this app user can enter the city name or state name and find out the weather conditions.",
                    image:require('../assets/image1.jpg'),
                    techstack:"HTML, CSS and Javascript has been used for frontend. Express,NodeJS has been used for backend. This app makes use of OpenWeatherMap APIs.On entering a valid username,the user is redirected to the page displaying the weather report and on invalid input, the user is taken to a 'Try Again' page.",
                    link:"https://radiant-wildwood-86842.herokuapp.com/"
                },
                {
                    id:2,
                    name:"To Do App",
                    desc:"Add your todo to a list so that you don't forget what your goals",
                    image:require('../assets/image2.jpg'),
                    techstack:"For the frontend, HTML,CSS and JavaScript has been used.Express, NodeJS and Mongoose have been used in backend.User can create a todo, mark it as completyed and also delete a todo.",
                    link:"https://github.com/SAY-droid427/toDoList"

                },
                {
                    id:3,
                    name:"BlogSite",
                    desc:"The user can compose the blog and publish them and also delete the blogs as per his/her wish. ",
                    image:require('../assets/image3.jpg'),
                    techstack:"For the frontend, HTML,CSS , Javascript and EJS has been used. For backend, Express, NodeJS and Mongoose has been used. The CRUD(Create, Read, Update, Delete) has been implemented in this app.",
                    link:"https://github.com/SAY-droid427/BlogsApp"
                
                },
                {
                    id:4,
                    name:"Chat With Docs",
                    desc:"It is modelled after Discord. Through this app, you can join a room and consult the doctor.",
                    image:require('../assets/image4.jpg'),
                    techstack:"For the frontend, vanillaJS has been used while for backend Express,NodeJS and scoket.io has been used.This app had been built as a part of our solution for 'Improving Lockdown Experience' for DevFest 1.0 organized by DevSoc BITS Goa.",
                    link:"https://arcane-sierra-51644.herokuapp.com/index.html"
                },
                {
                    id:5,
                    name:"Vue-Weather",
                    desc:"Enter the name of the city to know the weather.It also changes the background color according to the temperature",
                    image:require('../assets/image6.jpg'),
                    techstack:"This app has been built with Vue- a JavaScript framework and OpenWeatherMap API.I have tried to keep the background interactive.",
                    link:"https://github.com/SAY-droid427/vue-weather"
                },
                {
                    id:6,
                    name:"TEDx BITS Goa",
                    desc:"I had been one of the developers who had developed the official website for TEDx BITS Goa",
                    image:require('../assets/image7.jpg'),
                    techstack:"This website had been developed using HTML,CSS and JavaScript. Parallax has been used in this website. ",
                    link:"https://github.com/SAY-droid427/tedX-frontend"
                }
            ]
        }
    }
    
}
</script>
<style scoped>

</style>