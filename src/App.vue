<template>
  <div>
    <v-app>
      <Header />
      <v-main>
      <router-view />
    </v-main>
    <div>
    </div>
    <Footer />
    </v-app>    
  </div>
</template>
<script>
import Header from "./components/Header";
import Footer from "./components/Footer";
export default {
  name:"App",
  components:{
   Header,
   Footer
  },
  data:()=>({

  })
  
}
</script>
<style scoped>

</style>