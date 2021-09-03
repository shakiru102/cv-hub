<template>
  <div>
      <div class="main">
            <div class="contain mt-10">
                        <span class="cv">CV</span>
                        <span class="hub">HUB</span>
                        <!-- <span class="sec mx-2 hidden-sm-and-down">|</span>
                        <span class="text hidden-sm-and-down"></span>
                        <span class="cursor hidden-sm-and-down">_</span> -->
                        </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
 div.main{
     min-height: 60vh;
     display: flex;
     justify-content: center;
     align-items: center;
     /* background: rgba(255,255,255,.85) ; */
 }
.cv{
   text-align: center;
   background: rgb(27,33,89) ;
   padding: 20px;
   border-radius: 30px;
   color: rgba(255,255,255,.8) ;
    font-family: montserrat;
   font-size: 3em;
   font-weight:800;

}
.hub{
    color: rgb(27,33,89) ;
    margin-left:5px;
     font-family: montserrat;
   font-size: 3em;
   font-weight:800;
   /* 08124629222 */
}
</style>