<template>
    <div>
        <v-container>
            <v-container grid-list-xs>
            <v-row>
               <div class="black--text display-2"> Experience</div>
            </v-row>
            </v-container>
            <v-container>
                <v-row>
                    <v-col cols="12" v-for="item in items" :key="item.id">
                        <v-card :color="item.color">
                            <v-card-title>
                                {{item.name}}
                                <div class="font-weight-light">
                                    {{item.organization}}
                                </div>
                            </v-card-title>
                            <v-card-text class="white">
                                <div class="font-weight-bold">{{item.work}}</div>
                            </v-card-text>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-container>
    </div>
</template>
<script>
export default {
    name:"Experience",
    data(){
        return{
            items:[
                {
                    id:1,
                    name:"Senior Developer, ",
                    organization:"DevSoc(Developers' Society, BITS Goa)",
                    work:"Creating various websites and web applications for the college.I have created the website of TEDx BITS Goa in association with other web developers in DevSoc.",
                    color:"red lighten-2"
                },
                {
                    id:2,
                    name:"Software Developer, ",
                    organization:"Practice School Division, BITS Pilani",
                    work:"Developing and maintaining the Practice School Division, BITS Pilani website which is used by all the students of the college appearing and applying for PS-I and PS-II.",
                    color:"orange"

                }
            ]
        }
    }
}
</script>
<style scoped>

</style>