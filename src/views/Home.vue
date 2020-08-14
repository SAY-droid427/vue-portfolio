<template>
<div> 
       <v-parallax src="../assets/parallax.jpg" height="800">
       <div v-ripple class="text-center">
           <h1 class="black--text display-2">Hello!</h1>
           <h2 class="black--text display-3">I am Sayani Mallick!</h2>
           <h1 class="black--text">Student | Web Developer | Competitive Coder </h1>
           <h1 class="black--text display-1">I am an Electronics and Communication Engineering student in my sophomore year at BITS Pilani, K.K. Birla Goa Campus.I love solving problems using C++ and Python.I find delight in developing user-friendly and robust websites and web applications.I am also a painter and artist.</h1>
       </div>
       </v-parallax>
       <Aboutme />
     
</div>
</template>
<script>
import Aboutme from "../components/Aboutme"
export default {
    components:{
      Aboutme
    },
    data:()=>({

    })
}
</script>
<style scoped>
</style>