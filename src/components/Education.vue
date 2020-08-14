<template>
<v-container grid-list-xs>
    <v-container>
        <v-row>
            <div class="black--text display-2">Education</div>
        </v-row>
    </v-container>
    <v-divider></v-divider>
    <v-timeline>
        <v-timeline-item v-for="item in items" :key="item.id" :color="item.color" small>
          <template v-slot:opposite>
              <span :class="`headline font-weight-bold ${item.color}--text`" v-text="item.year">
              </span>
          </template>
          <div class="py-4">
           <h2 :class="`headline font-weight-bold mb-4 ${item.color}--text`">
             {{item.name}}
           </h2>
           <div>
             {{item.achievement}}
           </div>
          </div>

        </v-timeline-item>
    </v-timeline>
    <v-divider></v-divider>
</v-container>
</template>
<script>
export default {
    name:"Education",
    data(){
        return{
            items:[
                {
                    id:1,
                    name:"Birla Institute Of Technology and Sciences,Pilani",
                    year:"2019-2023(expected)",
                    achievement:"Electronics and Communication Engineering(8.19 CGPA)",
                    color:"red"
                },
                {
                    id:2,
                    name:"JVM Shyamali,Ranchi",
                    year:"2016-2018",
                    achievement:"Awarded for achieving the highest score in Physics in CBSE(95.8%)",
                    color:"green"
                },
                {
                    id:3,
                    name:"Bishop Westcott Girls' School",
                    year:"2012-2016",
                    achievement:"ICSE State Topper in Jharkhand(98.2%).Scored 100% in Mathematics and Computer Science.Scored 99%in Science and Social Sciences.",
                    color:"indigo"
                },
                {
                    id:4,
                    name:"St.Vincent's Convent School",
                    year:"2004-2012",
                    achievement:"Winner of Odisha-Chhattisgarh National Talent Search Examination conducted by ICSE.Also a House Captain in school.",
                    color:"orange"

                }
            ]
        }
    }
}
</script>
<style scoped>

</style>