<template>
  <div>
      <div class="foot">
            <v-container class="">
               <v-layout row wrap>
                 <v-flex xs12 md4 
                   v-for="details in footContent"
                  :key="details.title"
                  
                 >
                     <div class="subtitle font-weight-bold ml-4">{{details.title}}</div>
                     <v-row >
                       <!-- <v-col 
                       >
                       <v-row
                       v-for="(icon, iconindex) in details.icons "
                       :key="iconindex"
                       >
                          <v-icon color="grey" small>{{icon}}</v-icon>
                         </v-row>
                       </v-col> -->
                       <v-col>
                         <v-row
                          v-for="(cont, contindex) in details.content "
                       :key="contindex"
                         >
                           <div class="content mx-8 caption">{{cont}}</div>
                         </v-row>
                       </v-col>
                     </v-row>
                 </v-flex>
               </v-layout>
             </v-container>
      </div>
  </div>
</template>

<script>
export default {
  data:()=>({
    footContent:[
      {title:'ABOUT US',content:['Synergy between CODEFEST NIGERIA and SOFTWARESHOP LTD is the outcome of Computer VillageHub (CVHUB). An international development center on a mission to empower NIgerians digitally. A fully equipped with the right combination of tech professionals, tech resources and tech community. Co-Learning. Co-Workspace. Co-development. Co-llaboration.']},
      {title:'GET IN TOUCH',icons:['location_on','phone','mail'],content:['4B, Peppl Street, Beside Zenith Bank, Computer Village, Ikeja, Lagos','(+234) 8080808585','contact@cvhub4africa.com']},
      {title:'SHARE',date:['AUGUST 5, 2019','NOVEMBER 12, 2018','SEPTEMBER 24, 2018'],content:['Unearthing Destructive Habits in Business. Part 2','How To Overcome Business Failure Part1','Simple business Tips…Importance of Keeping Records']}
    ]
  })

}
</script>

<style scoped>
div.foot{
    min-height: 50vh;
    background: black;
    color:grey;
}

</style>