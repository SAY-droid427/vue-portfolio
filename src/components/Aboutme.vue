<template>
    <div>
        <Education />
       <Skills />
       <Experience />
    </div>
</template>
<script>
import Skills from "./Skills";
import Education from "./Education";
import Experience from "./Experience";
export default {
    name:"Aboutme",
    components:{
        Skills,
        Education,
        Experience
    }
}
</script>
<style scoped>
</style>