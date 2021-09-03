<template>
  <div>
      <div class="carouselContainer">
           <v-carousel
               cycle
               height="67vh"
               width="100%"
               hide-delimiter-background
               show-arrows-on-hover
               id="me"
             >
               <v-carousel-item 
               :key="image.title" v-for="image in homeImages"
               :src="require('@/assets/'+image.pic)"
               gradient="to top right , rgba(27,33,89,.6),rgba(27,33,89,.6)"
                >
                <v-sheet color="rgba(27,33,89,.0)"
                height="100%"
                
                >
                        <v-row
                        justify="center"
                align='center'
                class="fill-height"
                        >
                              <div class="words">
                                      {{image.title}}
                              </div>
                        </v-row>

                </v-sheet>
                
                
               </v-carousel-item>
             </v-carousel>
             <nav>
                  <v-app-bar color="rgb(0,0,0)" 
                  height="100px"
                  class="hidden-sm-and-down"
                  fixed
                   dark>
                          
                        <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->
                        <v-toolbar-title >
                            <div class="logo">
  <v-img 
                          
                          width="120px"
                          height="120px"
                          class="fit mt-5 mr-5" src="@/assets/Group (1).svg"></v-img>
                          </div>
                        </v-toolbar-title>
                        
                       <v-spacer></v-spacer>
                       <v-btn  text color="blue darken-1" v-for="nav in navs" :key="nav.name" :href="nav.link">
                         <v-icon></v-icon>
                         <span class="grey--text text--lighten-2">{{nav.name}}</span>
                       </v-btn>
                       <v-spacer></v-spacer>
                       <v-spacer></v-spacer>
                       <v-btn text color="blue darken-3">
                         <v-icon>exit_to_app</v-icon>
                         <span class="font-weight-bold">Login|Signup</span>
                       </v-btn>
                     </v-app-bar>
             </nav>            
         </div>
          <div class="tanime">
               <v-container class="">
                  <v-row>
                    <v-col
         
                    >
                        <div class="contain">
                        <span class="cv">CV</span>
                        <span class="hub">HUB</span>
                        <span class="sec mx-2 hidden-sm-and-down">|</span>
                        <span class="text hidden-sm-and-down"></span>
                        <span class="cursor hidden-sm-and-down">_</span>
                        </div>
                    </v-col>
                    <v-col>
                        <v-row >
                            <div class="mail hidden-xs-only">
                                <div class="mailanime">
                                 <v-icon  color="grey lighten-1">near_me</v-icon>
                                <span>
                                    <router-link
                                     class="mailto"
                                     to="mailto: contact@cvhub4africa.com">
                                         CONTACT@CVHUB4AFRICA.COM 
                                    </router-link>
                                </span>
                               </div>
                            </div>
                            <div class="mail hidden-sm-and-up">
                                <div class="mailanime2">
                                 <v-icon  color="grey lighten-1">near_me</v-icon>
                                <span>
                                    <router-link
                                     class="mailto2"
                                     to="mailto: contact@cvhub4africa.com" target="_blank">
                                         CONTACT@CVHUB4AFRICA.COM 
                                    </router-link>
                                </span>
                               </div>
                            </div>
                        </v-row>
                        <v-row
                        
                        justify="center"
                        align="center"
                        class="hidden-xs-only"
                        >
                             <span class="my-16 time">  <v-icon large color="grey lighten-1">
                                 access_time
                             </v-icon>
                               MON - SAT: 9:00AM - 6:00PM</span>
                        </v-row>
                    </v-col>
                  </v-row>
                  <v-row class="hidden-sm-and-up mt-16"
                  >
                      <v-col>
                           <span class="my-16 time">  <v-icon large color="grey lighten-1">
                                 access_time
                             </v-icon>
                               MON - SAT: 9:00AM - 6:00PM</span>
                      </v-col>
                  </v-row>
                </v-container>

             </div>
  </div>
</template>

<script>
import {gsap} from 'gsap'
import { TextPlugin } from "gsap/TextPlugin";
gsap.registerPlugin(TextPlugin);


export default {
    props:['homeImages'],
    data:()=>({
        navs:[
            {link:'/',name:'HOME',},
            {link:'/events',name:'EVENTS',},
            {link:'/',name:'SERVICES',},
            {link:'/course',name:'COURSE',},
            {link:'https://cvhub4africa.com/about-us/',name:'ABOUT US',},
            {link:'/',name:'TEAM',},
            {link:'/',name:'AMBASSADORS',},
            {link:'/',name:'CONTACT US',}

        ],
        text:['Bootcamp...','Incubation...','Co-workspace']
    }),
    mounted(){
        const words = this.text
        let mt = gsap.timeline({repeat:-1,repeatDelay:0.5})
        words.forEach(word => {
            let tl = gsap.timeline({yoyo:true,repeat:1,repeatDelay:1})
              tl.to('.text',{duration:1,text:word})
              mt.add(tl)
        });
        gsap.to('.cursor',{opacity:0,duration:0.5,repeat:-1,ease:'power(3)'})
        gsap.fromTo('.mailanime',{xPercent:-50, repeat:-1,duration:10},{xPercent:100, repeat:-1,duration:10})
    }

}
</script>

<style scoped>
.carouselContainer{
    position: relative;
    overflow: hidden;
}
nav{
    position: absolute;
    top: 0;
    width: 100%;
}

.fit{
    object-fit: contain;
}
div.words{
    font-family: montserrat;
    font-size: 5em;
    font-weight: bold;
    color: rgba(255,255,255,.3);
}
div.tanime{
    width: 100%;
    min-height: 33vh;
    background:rgb(27,33,89) ;
    position: relative;
}
div.contain{
    position: relative;
    top: 3em;
}
div .cv,.hub{
   font-family: montserrat;
   font-size: 3em;
   font-weight:800;

}
div .cv{
   text-align: center;
   background: rgba(255,255,255,.7);
   padding: 20px;
   border-radius: 30px;
   color:rgb(27,33,89) ;

}
div .hub{
    color: rgba(255,255,255,.7);
    margin-left:5px;
}
div .sec{
    color: rgba(255,255,255,.3);
    font-size: 4em;
    font-weight: lighter;
}
div .text{
    color: rgba(255,255,255,.3);
    font-size: 2em;

}
div.logo{
    position: relative;
    left: -2em;
}
div .cursor{
    color: rgba(255,255,255,.3);
    font-size: 2em;
    font-weight: bold;
}
div.mail{
    width: 100%;
    overflow: hidden;

}

span .mailto{
    text-decoration: none;
    color: rgba(255,255,255,.6);

}
span.time{
    color: rgba(255,255,255,.6);

}
.mailanime2{
    position: absolute;
    top: 0.5em;
    right: 1em;
}
.mailanime2 .mailto2{
    text-decoration: none;
    color: rgba(255,255,255,.6);

}

</style>