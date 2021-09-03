<template>
  <div>
      <div class="contain">
       <v-container class="">
         <v-layout row wrap>
           <v-flex xs12 md6>
             <div class="info1  my-16">
                 <v-card
                 dark
                     class="mx-16 hidden-xs-only anime"
                 elevation="24"
                     width="100%"
                     height="200px"
                     tile
                     color="rgb(27,33,89)"
                   >
                   <v-card-title>
                     <div class="tite grey--text text--lighten-2">
                       BOOTCAMP
                     </div>
                   </v-card-title>
                     
                     <v-card-text>
                       <div class="ti"></div>
                       <p class="grey--text text--lighten-1 pr-8">
                           An accelerated, target and product driven style of coaching students or trainees to achieve their personal goals with the aim of developing a product.
                      
                       </p>

                     </v-card-text>
                   </v-card>
                    <v-card
                 dark
                     class="hidden-sm-and-up"
                 elevation="24"
                     width="100%"
                     min-height="200px"
                     tile
                     color="rgb(27,33,89)"
                   >
                    <v-container class="">
                           <v-card-title>
                     <div class="tite grey--text text--lighten-2">
                       BOOTCAMP
                     </div>
                   </v-card-title>
                     
                     <v-card-text>
                       <div class="ti"></div>
                       <p class="grey--text text--lighten-1">
                           An accelerated, target and product driven style of coaching students or trainees to achieve their personal goals with the aim of developing a product.
                      
                       </p>

                     </v-card-text> 
                     </v-container>
                   </v-card>
             </div>
           </v-flex>
           <v-flex xs12 md6 class="hidden-sm-and-down">
             <div class="image imageone  my-16">
               <v-responsive>
                 <img 
                 width="100%"
                 height="350px"
                 class="  fit"
                 src="@/assets/Digital-Economy.jpg" alt="">
               </v-responsive>
               <div class="overlay">
                    <v-btn fab absolute
                    @click="color1='pink'"
                     large text class="" color="rgba(4, 3, 20, 0.788)" dark>
                           <v-icon 
                           :color="color1"
                            large dark >favorite</v-icon>
                         </v-btn>

               </div>
               <div class="overlay2">
                 
                   
               </div>
             </div>
           </v-flex> 
           <!-- CONTENT TWO -->
                      <v-flex xs12 md6 class="hidden-sm-and-down">
             <div class="image imagetwo  my-16">
               <v-responsive>
                 <img 
                 width="100%"
                min-height="200px"
                 class="fit"
                 src="@/assets/steps.jpg" alt="">
               </v-responsive>
               <div class="overlay">
                        <v-btn fab absolute
                    @click="color2='pink'"
                     large text class="" color="rgba(4, 3, 20, 0.788)" dark>
                           <v-icon 
                           :color="color2"
                            large dark >favorite</v-icon>
                         </v-btn>
               </div>
               <div class="overlay2">

               </div>
             </div>
           </v-flex>
                      <v-flex xs12 md6>
             <div class="info1  my-16">
                 <v-card
                 light
                     class="mx-16 hidden-xs-only anime1"
                 elevation="24"
                     width="100%"
                     height="200px"
                     tile
                     color="grey lighten-3"
                   
                   >
                   <v-card-title>
                     <div class="">
                      INCUBATION
                     </div>
                   </v-card-title>
                     
                     <v-card-text>
                       <div class="ti"></div>
                       <p class=" text--primary pr-8">
        An environment where ideas are birthed, housing it right from conception to when it becomes a full blown up project.
                      
                       </p>

                     </v-card-text>
                   </v-card>
                    <v-card
                 light
                     class="hidden-sm-and-up"
                 elevation="24"
                     width="100%"
                     height="200px"
                     tile
                     color="grey lighten-3"
                   >
                    <v-container class="">
                           <v-card-title>
                     <div class="tite ">
                       INCUBATION
                     </div>
                   </v-card-title>
                     
                     <v-card-text>
                       <div class="ti"></div>
                       <p class=" text--primary">
                            An environment where ideas are birthed, housing it right from conception to when it becomes a full blown up project.
                      
                       </p>

                     </v-card-text> 
                     </v-container>
                   </v-card>
             </div>
           </v-flex>
           <!-- CONTENT THREE -->
           <v-flex xs12 md6>
             <div class="info1  my-16">
                 <v-card
                 dark
                     class="mx-16 hidden-xs-only anime2"
                 elevation="24"
                     width="100%"
                     height="200px"
                     tile
                     color="rgb(27,33,89)"
                   >
                     <v-card-title>
                     <div class="tite grey--text text--lighten-2">                       
                      CO-WORKSPACE
                     </div>
                   </v-card-title>
                     <v-card-text>
                       <div class="ti"></div>
                       <p class="grey--text text--lighten-1 pr-8">
                         An environment where ideas are birthed, housing it right from conception to when it becomes a full blown up project.
                       </p>

                     </v-card-text>
                   </v-card>
                    <v-card
                 dark
                     class="hidden-sm-and-up"
                 elevation="24"
                     width="100%"
                    min-height="200px"
                     tile
                     color="rgb(27,33,89)"
                   >
                    <v-container class="">
                           <v-card-title>
                     <div class="tite grey--text text--lighten-2">
                     CO-WORKSPACE
                     </div>
                   </v-card-title>
                     
                     <v-card-text>
                       <div class="ti"></div>
                       <p class="grey--text text--lighten-1">
                           An environment where ideas are birthed, housing it right from conception to when it becomes a full blown up project.
                      
                       </p>

                     </v-card-text> 
                     </v-container>
                   </v-card>
             </div>
           </v-flex>
           <v-flex xs12 md6 class="hidden-sm-and-down">
             <div class="image imagethree my-16">
               <v-responsive>
                 <img 
                 width="100%"
                 height="350px"
                 class="fit"
                 src="@/assets/kid.jpg" alt="">
               </v-responsive>
               <div class="overlay">
                    <v-btn fab absolute
                    @click="color3='pink'"
                     large text class="" color="rgba(4, 3, 20, 0.788)" dark>
                           <v-icon 
                           :color="color3"
                            large dark >favorite</v-icon>
                         </v-btn>

               </div>
               <div class="overlay2">
                 
                   
               </div>
             </div>
           </v-flex>
           <!-- CONTENT FOUR -->
                       <v-flex xs12 md6 class="hidden-sm-and-down">
             <div class="image imagefour my-16">
               <v-responsive>
                 <img 
                 width="100%"
                 height="350px"
                 class="fit"
                 src="@/assets/code.jpeg" alt="">
               </v-responsive>
               <div class="overlay">
                        <v-btn fab absolute
                    @click="color2='pink'"
                     large text class="" color="rgba(4, 3, 20, 0.788)" dark>
                           <v-icon 
                           :color="color2"
                            large dark >favorite</v-icon>
                         </v-btn>
               </div>
               <div class="overlay2">

               </div>
             </div>
           </v-flex>
                      <v-flex xs12 md6>
             <div class="info1  my-16">
                 <v-card
                 light
                     class="mx-16 hidden-xs-only anime3"
                 elevation="24"
                     width="100%"
                     height="200px"
                     tile
                   color="grey lighten-3"  
                   
                   >
                                      <v-card-title>
                     <div class="">
                      HACKATHON
                     </div>
                   </v-card-title>
                     
                     <v-card-text>
                       <div class="ti"></div>
                       <p class=" text--primary pr-8">
        A design sprint-like event in which computer programmers and others involved in software development, including graphic designers, interface designers, project managers, and others, often including subject-matter-experts, collaborate intensively on software projects.
                      
                       </p>

                     </v-card-text>

                   </v-card>
                    <v-card
                 light
                     class="hidden-sm-and-up"
                 elevation="24"
                     width="100%"
                     min-height="200px"
                     tile
                     color="grey lighten-3"
                   >
                    <v-container class="">
                           <v-card-title>
                     <div class="tite ">
                       HACKATHON
                     </div>
                   </v-card-title>
                     
                     <v-card-text>
                       <div class="ti"></div>
                       <p class=" text--primary">
                          A design sprint-like event in which computer programmers and others involved in software development, including graphic designers, interface designers, project managers, and others, often including subject-matter-experts, collaborate intensively on software projects.
                      
                       </p>

                     </v-card-text> 
                     </v-container>
                   </v-card>
             </div>
           </v-flex>
         </v-layout>
        </v-container>
      </div>
      
  </div>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
export default {
  data:()=>({
    color1:'white',
    color2:'white',
    color3:'white',
    color4:'white',
  }),
  mounted(){
    gsap.from('.anime.v-card',{scrollTrigger:{
      trigger:'.anime.v-card',
      start:'center bottom',
      // toggleActions:'play none restart none'
    },duration:0.5,xPercent:-100, scale:0.5,  ease:'power',opacity:0});
        gsap.from('.anime1.v-card',{scrollTrigger:{
      trigger:'.anime1.v-card',
      start:'center bottom',
      // toggleActions:'play none restart none'
    },duration:0.5,xPercent:100, scale:0.5,  ease:'power',opacity:0});
        gsap.from('.anime2.v-card',{scrollTrigger:{
      trigger:'.anime2.v-card',
      start:'center bottom',
      // toggleActions:'play none restart none'
    },duration:0.5,xPercent:-100, scale:0.5,  ease:'power',opacity:0});
        gsap.from('.anime3.v-card',{scrollTrigger:{
      trigger:'.anime3.v-card',
      start:'center bottom',
      // toggleActions:'play none restart none'
    },duration:0.5,xPercent:100, scale:0.5,  ease:'power',opacity:0});
    gsap.from('.imageone',{scrollTrigger:{
      trigger:'.imageone',
      start:'top bottom',
      // toggleActions:'play none restart none'
    },yPercent:100,duration:0.5,ease:'power(4)',opacity:0});
        gsap.from('.imagetwo',{scrollTrigger:{
      trigger:'.imagetwo',
      start:'top bottom',
      // toggleActions:'play none restart none'
    },xPercent:-100,duration:0.5,ease:'power(4)',opacity:0,delay:0.4});
      gsap.from('.imagethree',{scrollTrigger:{
      trigger:'.imagethree',
      start:'top bottom',
    },yPercent:-100,duration:0.5,ease:'power(4)',opacity:0,delay:0.4});
    gsap.from('.imagefour',{scrollTrigger:{
      trigger:'.imagefour',
      start:'top bottom',
    },yPercent:100,duration:0.5,ease:'power(4)',opacity:0});
    
  }
  


}
</script>

<style scoped>
.contain{
    min-height: 100vh;
    width: 100%;
    background:url('../assets/cvhubstyle 5.svg')
    ;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
}
div.info1{
   height: 350px;
   display: flex;
   justify-content: center;
   align-items: center;
  width: 100%;
  transition: 0.4s ease-in-out;
}
/* div.info1:hover{
  transform: scale(1.05);
} */
div.image{
  height: 350px;
  position: relative;
  overflow: hidden;
  box-shadow: 0px 5px 24px black;
}
div.image:hover div.overlay{
  top: 0;
}
div.image:hover div.overlay2{
  top: 100%;
}
div.overlay{
  position: absolute;
  top: 100%;
  left: 0;
  transition: 0.2s ease-in-out;
  width: 100%;
min-height: 350px;
  background: rgba(12, 9, 48, 0.788);
  display: flex;
  justify-content: center;
  align-items: center;
}
div.overlay2{
  position: absolute;
  top: 0;
  left: 0;
  transition: 0.2s ease-in-out;
  width: 100%;
  min-height: 350px;
  background: rgba(27,33,89,.2);
  
}
img.fit{
  object-fit: cover;
}
div.ti{
   width: 15%;
   height: 2px;
   background: orange;
   position: relative;
   top: -0.6em;
}

</style>