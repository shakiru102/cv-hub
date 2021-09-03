<template>
  <div>
  <div class="overb">
     <div class="parent" id="cv">
         <Carousel :homeImages="homeImages"/>
       <div class="pointTwo">
         <div class="point">
           <Content/>
         </div>
         <div>
          <ContentTwo/>
         </div>
         <div>
           <ContentThree/>
         </div>
          <div >
          <ContentFour/>
         </div>
         <span class="fixed hidden-md-and-up">
            <v-btn small elevation="24"
            href="#cv"
             color="red"
             class="mt-7 b mr-3 "
              fab>  <v-icon small color="white">arrow_upward</v-icon>
             </v-btn>
        
      </span>
      <div class="space">
        
      </div>
         </div>
        
     </div>
     </div>
  </div>
</template>

<script>

import Carousel from '@/components/carousel'
import Content from '../components/content.vue'
import ContentTwo from '@/components/contentTwo'
import ContentThree from '@/components/contentThree'
import ContentFour from '@/components/contentFour'
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
 
export default {
  components: { 
    Carousel,
    Content,
    ContentTwo, 
    ContentThree,
    ContentFour
    },
  data:()=>({
    homeImages:[
      {pic:'learn.jpg',title:'LEARN'},{pic:'think.jpg',title:"THINK"},{pic:'innovate.jpg',title:'INNOVATE'}
    ],
    navs:[
            {link:'/',name:'HOME',},
            {link:'/events',name:'EVENTS',},
            {link:'/',name:'SERVICES',},
            {link:'/course',name:'COURSE',},
            {link:'https://cvhub4africa.com/about-us/',name:'ABOUT US',},
            {link:'/',name:'TEAM',},
            {link:'/',name:'AMBASSADORS',},
            {link:'/',name:'CONTACT US',}

        ]
  }),
  mounted(){
    let tl = gsap.timeline({scrollTrigger:{
      trigger:'.point',
      start:'top top'
    }})
    tl.from('.b.v-btn',{y: 100, duration: 0.5, opacity: 0, ease:'back(5)'});
    // let tl1 = gsap.timeline({scrollTrigger:{
    //   trigger:'.pointTwo',
    //   start:'bottom top'
    
    // }})
    // tl1.to('.fixed',{opacity: 0, duration: 0.1})
  
  
  }

}
</script>

<style scoped>
div.pointTwo{
  position: relative;
}
span.fixed{
  position:sticky;
  bottom: 3em;
  left: 78em;
  
}
.test{
  height: 100vh;
}
#cv{
     background: rgba(255,255,255,.85) ;

}
div.overb{
background: rgb(27,33,89) ; 
}
div.space{
  height: 1em;
}

</style>