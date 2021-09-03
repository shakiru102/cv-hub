<template>
  <div>
      <div class="panel hidden-md-and-up">
        <v-expansion-panels
            dark
            tile
        
        >
          <v-expansion-panel
          
          >
            <v-expansion-panel-header
             expand-icon="menu"
             disable-icon-rotate
             color="black"
            >
              <div class="logo">
              <v-img 
               width="120px"
                          height="100%"
                          class="fit mt-1 " src="@/assets/Group (1).svg"
              ></v-img>
              </div>
            </v-expansion-panel-header>
            <v-expansion-panel-content 
            color="rgb(27,33,89)">
               <v-list color="rgb(27,33,89)">
                 <v-list-item :key="nav.name" v-for="nav in navs" :href="nav.link">
                   <v-list-item-content >
                    <div class=" hidden-xs-only ">
                      {{nav.name}}
                    </div>
                    <div class=" hidden-sm-and-up caption ">
                      {{nav.name}}
                    </div>
                   </v-list-item-content>
                 </v-list-item>
               </v-list>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
          
      </div>
  </div>
</template>

<script>
export default {
  data:()=>({
    navs:[
            {link:'/',name:'HOME',},
            {link:'/events',name:'EVENTS',},
            {link:'/',name:'SERVICES',},
            {link:'/course',name:'COURSE',},
            {link:'/',name:'ABOUT US',},
            {link:'/',name:'TEAM',},
            {link:'/',name:'AMBASSADORS',},
            {link:'/',name:'CONTACT US',}

        ],
  })

}
</script>

<style scoped>
div.panel{
  position: relative;
}
div.logo{
 height: 40px;
 width: 50px;
 position: relative ;
 left: -4em;
}

</style>