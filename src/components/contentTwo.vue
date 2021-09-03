<template>
  <div>
      <div class="image">
        <div class="move">
        <v-img height="50vh"  class="" contain src="@/assets/get_start-removebg-preview.png"></v-img>
        </div>
      </div>
    
         <v-carousel
            cycle
             height="100vh"
             hide-delimiter-background
             show-arrows-on-hover
             delimiter-icon="mdi-minus"
             interval="9000"
           >
             <v-carousel-item 
             v-for="course in courses"
             :key="course.title"
            :src="course.src"
            gradient="to top right , rgba(27,33,89,.95),rgba(27,33,89,.95)"
            class="trans"
            color="rgb(27,33,89)"
             >
             <div class="content">
                <v-card
                    class="hidden-xs-only mt-12"
                elevation="24"
                    width="50%"
                  
                  >
                  <v-img :src="course.src" height="400px" width="100%"></v-img>
                  
                    <v-card-text>
                      <p class="">
                       <span class="mx-2" v-for="icon in course.icons" :key="icon.name" > <v-icon small color="orange">{{icon.name}}</v-icon>
                       {{icon.iconText}} 
                       </span>
                      </p>
                      <div class="grey--text">
                       {{course.content}}
                      </div>
                    </v-card-text>
                    <v-card-actions>
                      <v-btn
                        tile
                        color="blue"
                        :href="course.link"
                        target="_blank"
                      >
                       <span>APPLY NOW</span>
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                                  <v-card
                    class="hidden-sm-and-up"
                elevation="24"
                    width="100%"
                  
                  
                     >
                  <v-img :src="course.src" height="250px" width="100%"></v-img>
                  
                    <v-card-text>
                      <p class="">
                       <span class="mx-2" v-for="icon in course.icons" :key="icon.name" > <v-icon small color="orange">{{icon.name}}</v-icon>
                       {{icon.iconText}} 
                       </span>
                      </p>
                      <div class="grey--text">
                       {{course.content}}
                      </div>
                    </v-card-text>
                    <v-card-actions>
                      <v-btn
                        tile
                        color="blue"
                        :href="course.link"
                        target="_blank"
                      >
                       <span>APPLY NOW</span>
                      </v-btn>
                    </v-card-actions>
                  </v-card>
                  <span class="popularCourse display-1 mt-7">POPULAR COURSE </span>
               </div>
             </v-carousel-item>
             <v-carousel-item
               
             >
             <v-sheet
             dark
             width="100%"
             height="100%"
              >
              <div class="parent">
               <v-container class="" >
                  <v-layout row wrap>
                    <v-flex sm6 md4  v-for="(image, imageIndex) in courseImages" :key="imageIndex">
                     <v-card 
                         class="mx-2 mt-6"
                     elevation="24"
                        height="250px"
                         dark
                        
                        
                       >
                         
                         <v-img class="" :src="image" height="100%" width="100%"></v-img>
                         
                       </v-card>
                    </v-flex>
                  </v-layout>
                </v-container>
                <div class="moreCourses">
                      <v-btn large elevation="24" class="" color=" primary">VIEW MORE COURSES</v-btn>
                  
                </div>
                </div>
              </v-sheet>
             
             </v-carousel-item>
           </v-carousel>
  </div>
</template>

<script>
export default {
  data:()=>({
    courses:[
      {
        src:'https://cvhub4africa.com/wp-content/uploads/2020/02/Mobile-App-Development-Nigerira.png',
        title:'DEVELOPERS HANGOUT',
        content:'XAMARIN + FIREBASE: Making Beautiful & Powerful Mobile app',
        link:'https://cvhub4africa.com/course/mobile-apps-develop/developers-hangout/',
        icons:[
          {name:'calendar_today',iconText:'8:00AM-12:00PM'},
          {name:'person',iconText:'PHILIP CHUKWUKA AMAMCHUKWU'},
          {name:'school',iconText:'BEGINNER'}
    ]

      },
          {
        src:'https://cvhub4africa.com/wp-content/uploads/2020/03/Scientific-Python-Scipy-696x500.jpg',
        title:'PROGRAMMING IN PYTHON',
        content:'This is the first course in Python Certificate program which is a 9-month curriculum.',
        link:'https://cvhub4africa.com/course/mobile-apps-develop/programming-in-python/',
        icons:[
          {name:'calendar_today',iconText:'10 WEEKS'},
          {name:'school',iconText:'BEGINNER'}
    ]

      },

    ],
    courseImages:[
      'https://cvhub4africa.com/wp-content/uploads/2016/01/ICT-Buider.png',
      "https://cvhub4africa.com/wp-content/uploads/2016/01/Made-in-Ikeja.png",
      "https://cvhub4africa.com/wp-content/uploads/2019/03/VIDEO-EDITING-Banner_4-1.png",
      "https://cvhub4africa.com/wp-content/uploads/2019/02/DIGITAL-MARKETING-Banner-Online_1.png",
      "https://cvhub4africa.com/wp-content/uploads/2019/09/1352468_3d97_3.jpg",
      "https://cvhub4africa.com/wp-content/uploads/2019/09/520116_edf5_2.jpg",


    ]
  })

}
</script>

<style scoped>
.image{
    width: 100%;
    min-height: 80vh;
    background: rgb(27,33,89);
    /* background:linear-gradient(to top right , rgba(27,33,89,.95),rgba(27,33,89,.95)), url('../assets/get_start.jpg');
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
     */
}
.move{
  position: relative;
  top: 7em;
}
.content{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  /* background:linear-gradient(to right,rgba(27,33,89,.9),rgba(27,33,89,.9)), url('../assets/app.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center; */
    
}
span.popularCourse{
  position: absolute;
  color: whitesmoke;
  text-shadow: 0px 5px 4px black;
  /* color: rgba(186, 187, 190, 0.808); */
  top: 0;
}
.parent{
  position: relative;
  height: 100%;
}
.moreCourses{
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: rgba(8,7,32,.5);
}

</style>