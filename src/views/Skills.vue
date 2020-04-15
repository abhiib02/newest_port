<template>
    <div class="fullvh">

        <div class="grid-container">
            <div class="top">
                <vueper-slides
                    style="width:100%"
                    class="no-shadow"
                    :autoplay="true"
                    :bullets="false"
                    :infinite="true"
                    :visible-slides="6"
                    slide-multiple
                    :gap="3"
                    :slide-ratio="resp()"
                    :dragging-distance="200"
                    
                    :breakpoints="{ 500: { visibleSlides: 2, slideMultiple: 2 } }"
                    >
                  <vueper-slide class="card" v-for="(skill, i) in skills" :key="i" >
                      <template v-slot:content>
                          
                          <img :src="skill.techlogo">
                          <h4>{{skill.tech}}</h4>
                        <!------------------------------------------>

                        <svg width="50" height="50" xmlns="http://www.w3.org/2000/svg">

  <ellipse ry="23" rx="23" id="svg_1" cy="24.846565" cx="24.81035" stroke-dasharray="144.44" :stroke-dashoffset="percentage(skill.per)" stroke-width="2" stroke="#000" fill="none"/>
    <text x="50%" y="50%" text-anchor="middle" stroke="#000000" stroke-width="1px" dy=".2em">{{skill.per}}%</text>
</svg>

                        <!------------------------------------------>
                           
                        </template>
                  </vueper-slide>

                </vueper-slides>
                <!--<div class="rightTI li">
                     <div class="marqwrapper">
                        <div v-for="skill in skills" :key="skill">
                            <img width="96px" height="96px" :src="skill.techlogo">
                            <h3>{{skill.tech}}</h3>
                            <hr :style="perwidth(skill.per)">
                           
                        </div>
                    </div>
                </div>-->
               <!-- <marquee behavior="alternate" scrollamount="1"   direction="">
                    <div class="marqwrapper">
                        <div v-for="skill in skills" :key="skill">
                            <img width="96px" height="96px" :src="skill.techlogo">
                            <h2>{{skill.tech}}</h2>
                        </div>
                    </div>
                </marquee>-->
            </div>
            <div class="bottom">
                 <p class="heading text-left text-white">Skills</p>
                 <p class="desc text-white">These are the technologies i have worked with.
All these technologies consist of frontend technologies like (HTML,CSS,JAVASCRIPT) Backend technologies like (PHP,ASP.NET) and Database technology(MySQL).
I am familiar with some useful framework like FrontEnd Framework (Bootstrap,Bulma,MaterializeCSS), and BackEnd Framework (Codeigniter,Laravel). </p>
            </div>
        </div>

    </div>
</template>
<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'
    export default {
        components: { VueperSlides, VueperSlide },
        data() {
            return {
                skills: [
                    {
                        techlogo: 'https://img.icons8.com/color/2x/html-5.png',
                        tech: 'HTML',
                        per:90
                    },
                    {
                        techlogo: 'https://img.icons8.com/color/2x/css3.png',
                        tech: 'CSS3',
                        per:85
                    },
                    {
                        techlogo: 'https://upload.wikimedia.org/wikipedia/en/thumb/6/62/MySQL.svg/1150px-MySQL.svg.png',
                        tech: 'MySQL',
                        per:50
                    },
                    {
                        techlogo: 'https://www.prchecker.info/free-icons/128x128/php_128_px.png',
                        tech: 'PHP',
                        per:50
                    },
                    {
                        techlogo: 'https://img.icons8.com/color/2x/javascript.png',
                        tech: 'Javascript',
                        per:50
                    },
                    {
                        techlogo: 'https://cdn.iconscout.com/icon/free/png-256/jquery-10-1175155.png',
                        tech: 'Jquery',
                        per:50
                    },
                    {
                        techlogo: 'https://cdn1.iconfinder.com/data/icons/logos-3/304/codeigniter-icon-512.png',
                        tech: 'CodeIgniter',
                        per:60
                    },
                    {
                        techlogo: 'http://obscureproblemsandgotchas.com/wp-content/uploads/2018/06/bootstrap-stack-e1530246058846.png',
                        tech: 'Bootstrap',
                        per:70
                    },
                    {
                        techlogo: 'https://formvalidation.io/branches/bulma.svg',
                        tech: 'Bulma',
                        per:40
                    },
                    {
                        techlogo: 'https://www.consolebit.com/media/technologies/logo-materialize.png',
                        tech:'Materialize CSS',
                        per:70
                    },
                    {
                        techlogo: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Laravel.svg/220px-Laravel.svg.png',
                        tech: 'Laravel',
                        per:50
                    },
                    {
                        techlogo: 'https://www.stickpng.com/assets/images/58482acecef1014c0b5e4a1e.png',
                        tech: 'Vue JS',
                        per:50
                    },
                    {
                        techlogo: 'https://cdn.freebiesupply.com/logos/large/2x/nativescript-logo-png-transparent.png',
                        tech: 'NativeScript',
                        per:30
                    },
                    {
                        techlogo: 'https://sass-lang.com/assets/img/styleguide/seal-color-aef0354c.png',
                        tech: 'Sass (SCSS)',
                        per:70
                    },

                ],
                x: '',
                y: ''
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
                return 'transform:translate(' + -this.x + 'px,' + -this.y + 'px);';
            },
            
            
        }
    }
</script>
<style lang="scss" scoped>
    img{
        width:70px;
        height:70px;
    }
    .grid-container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        grid-template-areas: "top top top top""bottom bottom bottom bottom";
        margin:0px 53px;
        
    }

    .top {
        grid-area: top;
        display:flex;
        flex-wrap: wrap;
        justify-content: center;
        margin:auto 0;
        
    }

    .bottom {
        margin:auto 0;
        grid-area: bottom;
    }
    marquee{
        scroll-behavior: smooth;
    }
    .marqwrapper{
        display: flex;
        flex-direction: row;
        
        div{
            max-width:180px;
            max-height:250px;
             min-width:180px;
            min-height:250px;
            margin:10px;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            background: white;
            color:white;
            border-radius: 8px;
            background: linear-gradient(144.25deg, #fff, #f00 100% );
            box-shadow: 2px 2px 10px #000;
            transition: all .5s ease;
            hr{
                margin:0;
                padding: 0;
                transform-origin: left;
               width:0%;
                height: 10px;
                background:#000;
                color:#000;
                border-radius:50px;
            }
        }
    }
   
  .rightTI { 
      width:auto;
    white-space: nowrap; 
    overflow: scroll;
    animation: marquee 10s linear infinite alternate;
}
.rightTI:hover {
  animation-play-state: paused;
  
}
@-webkit-keyframes marquee {
  0% {transform: translateX(0%);}
  100% {transform: translateX(-100%);}
}
.card{
            
            width:33.33%;
            height:250px;
            margin:10px;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            background: white;
            color:white;
            border-radius: 8px;
            background: linear-gradient(144.25deg, #fff, #f00 100% );
            box-shadow: 2px 2px 10px #000;
            transition: all .5s ease;
            hr{
                margin:0;
                padding: 0;
                transform-origin: left;
                width:0%;
                height: 10px;
                background:#000;
                color:#000;
                border-radius:50px;
            }
        }
@media screen and (max-width: 700px) {
    .grid-container{
        display: flex;
        flex-direction: column;
        margin:0;
    }
    .top{
        margin-top:60px;
        width: 100%;
    }
    .text-left{
        text-align: center;
    }
    .bottom{
        text-align: justify;
        
    }
    .desc{
        font-size: 14px;
    }
    img{
        width:40px;
        height:40px;
    }
}
</style>