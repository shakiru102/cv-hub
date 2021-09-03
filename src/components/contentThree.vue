<template>
  <div>
      <div class="parent">
         <div class="header">
           <v-container class="">
            
                  <div class="display-1 white--text text-center mt-6 ">
                    LATEST TECH NEWS
                  </div>
              
            </v-container>
         </div>
         <div  class="newsContent mt-8 ">
            <v-container class="">
              <v-layout row wrap 
              justify-space-around
              >
                <v-flex
                sm6
                md4
                
                 v-for="article in articles" :key="article.title">
                  <v-card
                      class="mx-2 my-6 hov"
                  elevation="24"
                      height="700px"
                      dark
                    >
                    <v-img width="100%" :src="article.urlToImage" 
                    height="250px"
                    ></v-img>
                      <div class="title px-5">
                       {{article.title}}
                      </div>
                      
                      <v-card-text>
                        <p class="">
                         {{article.description}}
                        </p>
                        <div class="caption">
                         <span>{{article.author}}</span>
                         <v-spacer></v-spacer>
                         <span>{{article.publishedAt}}</span>
                        </div>
                      </v-card-text>
                      <v-card-actions>
                        <v-btn
                          text
                          color="primary"
                          :href="article.url"
                          target="_blank"
                        >
                         <span >READ MORE</span>
                        </v-btn>
                      </v-card-actions>
                    </v-card>
                </v-flex>
              </v-layout>
             </v-container>
         </div>
      </div>
  </div>
</template>

<script>

export default {
  data:()=>({
      articles:[],
      api:'https://newsapi.org/v2/top-headlines?sources=techcrunch&apiKey=58e517f1d9f845deb2ffc9fa214e300d'
  }),
  created(){
    this.$http.get(this.api).then(function(data){
      return data.json()
    }).then(function(data){
             this.articles = data.articles
             console.log(this.articles)
    }).catch(e => {
      console.error(e)
    })
    
  },

}
</script>

<style scoped>
 .parent{
     min-height: 100vh;
     width: 100%;
    background: rgb(27,33,89);

 }
.hov.v-card{
   transition: 0.5s ease-in-out;
}
 .hov.v-card:hover{
   transform: translateY(-25px);
 }
 div.header{
  text-shadow: 0px 5px 4px black;

 }

</style>