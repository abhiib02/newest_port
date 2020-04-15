<template>
  <div class="fullvh"  >
      <div class="grid" >
          <div class="left">
              <p class="heading text-left text-white">About Me</p>
              <p class="desc text-white">My name is <span class="text-red">Abhishek Bhardwaj</span> and i am 
                                {{ new Date().getFullYear()-1995 }} Years old, i have a polytechnic diploma in <span class="text-red">electronics and communication engineering</span> which was completed in the year of 2017, i also have a Degree of <span class="text-red">Bachelors of
                            computer application</span> from IGNOU in the year of 2018, i am a tech enthusiast who want to know about new technologies but more interested in<span class="text-red"> website designing and development</span>,i also maintain a facebook page with around thousand
                            likes i also manage tech blog mention inside projects, i like to play video game and listening songs,to Know More About me there are navigation links.</p>
          </div>
          <div class="right"  >
               <img src="https://graph.facebook.com/100005873828354/picture?width=400&amp;height=400" alt="">
          </div>
      </div>
  </div>
</template>
<script>
export default {
    data(){
        return {
            x:'',
            y:''
        }
    },
    methods: {
            mouseinvert(event) {

                var x3d, y3d;
                x3d = event.clientX - (window.innerWidth * 0.5);
                y3d = event.clientY - (window.innerHeight * 0.5);
                x3d = x3d * 0.2;
                y3d = y3d * 0.2;
                this.x = x3d;
                this.y = y3d;
            },
            perwidth(per){
                return 'transform:scaleX('+per+'%)';
            },
            percentage(val){
                return  144.44 - (1.4444 * val) ;
            },
            resp(){
               if(window.innerWidth <= 500){
                   return 1;
               }
               if(window.innerWidth >501){
                   return 1/4;
               }
            }
        },
        computed: {
            invertranslate() {
                return 'box-shadow:'+this.x+'px '+this.y+'px 10px #FF0000;';
            },
            
            
        }
}
</script>
<style lang="scss" scoped>
 .grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr;
        grid-template-areas: "left right";
        height: 100%;
    }

    .left {
        grid-area: left;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding:0px 20px;

    }

    .right {
        grid-area: right;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        img{
            mix-blend-mode: normal;
            backdrop-filter: blur(0px);
            border-radius: 50%;
            box-shadow: 0px 0px 10px #FF0000;
            filter: brightness(0.8) blur(0);
transform: matrix(-1, 0, 0, 1, 0, 0);
        }
    }
@media screen and (max-width: 700px) {
    .grid{
        display: flex;
        flex-direction: column-reverse;
    }
    .right{
        img{
            width:60%;
            
        }
    }
    .desc{
        font-size: 12px;
    }
}

</style>