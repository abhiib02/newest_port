<template>

  <div id="app">
  <Navigation/>
  <transition name="fade" mode="out-in">
    
 
    <router-view></router-view>
   </transition>
  </div>    

   
</template>

<script>
import Navigation from '@/components/Navigation.vue'

export default {
  components:{
    Navigation,
    
  },
   data(){
    return{
    }}
}
</script>
<style lang="scss">
.fade-enter{transform: translateX(-50%);opacity: 0;}
.fade-enter-to{transform: translateX(0);opacity: 1;}
.fade-enter-active{
  transition: all 1s ease;
}
.fade-leave{transform: translateX(0%);opacity: 1;}
.fade-leave-to{transform: translateX(50%);opacity: 0;}
.fade-leave-active{
  transition: all 1s ease;
}
body{
  margin:0;
  background: #0f0f0f;
  background-image:url('./assets/imgs/dots.svg');
  background-attachment: fixed;
  background-repeat: no-repeat;
  background:cover;
  overflow-x: hidden;
  font-family: Montserrat;
  animation: anim 5s linear infinite alternate;
}
hr{
  width:70%;
  color:white;
}
@keyframes anim{
0%{background-position-x:50%;

    }
100%{background-position-x:10%;
}
}

.fullvh{
  margin-left: 70px;
  padding:0px 10px;
  widows: 100%;
  height: 100vh;
  
}

.flex-row{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
.flex-col{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.button{
  width:100px;
  height: auto;
  border: 0;
  padding:10px 0px;
  color:#fff;
  margin:0px 10px;
  border-radius: 5px;
  text-align: center;
  text-decoration: none;
}
.button-2{
  width:100px;
  height: auto;
  border: 2px solid red;
  padding:10px 0px;
  background: transparent;
  color:#fff;
   margin:0px 10px;
   border-radius: 5px;
   text-align: center;
  text-decoration: none;
}
.red{
  background: #ff0000;
}
.heading {
        font-size: 64px;
        width: 100%;
        margin: 0;
        
        
    }
    .desc{
      font-size: 24px;
      
      text-align: justify;
      
    }
    .text-left{text-align:left;}
    .text-right{text-align:right;}
    .text-center{text-align:center;}
    .text-red {color: #f00 !important;}
    .text-white{color: #fff !important;}
@media screen and (max-width: 600px) {
  .fullvh{
  margin: 0;
  
  }
 
  .heading {
        font-size: 2rem;
        width: 100%;
        margin: 0;
        
        
    }
}
</style>
