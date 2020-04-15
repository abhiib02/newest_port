<template>

  <div class=" fullvh">
    
    <div class="wrapper">
      
      <p class="heading text-left text-white">Work</p>
        <div>
          <img src="@/assets/imgs/bsm.jpg" alt="">
          <div>BackStageMumbai.in
            <hr>
            HTML | CSS | JS
          </div>
        </div>
        <div>
          <img src="@/assets/imgs/dexo.jpg" alt="">
          <div>Dexo.Media
            <hr>
            HTML | CSS | JS
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/dynamo.jpg" alt="">
          <div>DynamoHack.Blogspot.com
            <hr>
            HTML | CSS | BLOGGER
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/gang.jpg" alt="">
          <div>Gangmy.Design
            <hr>
            HTML | CSS | WORDPRESS | JS 
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/gyb.jpg" alt="">
          <div>GYBindia.in
            <hr>
            HTML | CSS | JS
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/madan.jpg" alt="">
          <div>MadanFashion.in
             <hr>
            HTML | CSS | WORDPRESS | JS 
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/pp.jpg" alt="">
          <div>PetitePebble.com
            <hr>
            HTML | CSS | JS
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/scc.jpg" alt="">
          <div>SCC-education.com
            <hr>
            HTML | CSS | BLOGGER
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/uc.jpg" alt="">
          <div>UnitedChemical.in
            <hr>
            HTML | CSS | JS
          </div>
          </div>
        <div>
          <img style="width:37%" src="@/assets/imgs/splogo.png" alt="">
          <div>Sachin Packaging App
            <hr>
            HTML | CSS | VUE | NativeScript
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/vb.jpg" alt="">
          <div>VoyagerBeat.com
            <hr>
            HTML | CSS | JS | CODEIGNITOR 
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/vwt.jpg" alt="">
          <div>VictoryWorldTourism.com
            <hr>
            HTML | CSS | JS | LARAVEL 
          </div>
          </div>
        <div>
          <img src="@/assets/imgs/wci.jpg" alt="">
          <div>WoodCraftInt.com
            <hr>
            HTML | CSS | JS
          </div>
          </div>

      

    </div>
  </div>

</template>
<script>
  export default {
    data() {
      return {

      }
    },
    methods: {

    },
    computed: {
      cursorimg(event) {
        return 'top:' + event.clientY + 'px;left:' + event.clientX + 'px;';
      }
    }

  }
</script>
<style lang="scss" scoped>
  body {
    overflow-x: hidden;
    overflow: scroll;
  }
 
  .wrapper {
    display: flex;
    flex-direction: row;
    padding-top: 60px;
    flex-wrap: wrap;
  
    div {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      flex-direction: column;
      padding:10px 0px;
      width: 33.33%;
      height: 300px;
      img{
        width:90%;
        height: auto;
        box-shadow: 0px 0px 10px #000;
        z-index:900;
        border-radius: 10px;
      }
      div{
        width:80%;
        height: 100%;
        background: white;
        color:#fff;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        background: linear-gradient(90deg, #000000 0%, #000000 0%, #FF0000 100%);
      }
      

    }
  }
  @media screen and (max-width: 900px) {
     .wrapper {
    display: flex;
    flex-direction: row;
    
    flex-wrap: wrap;
  
    div {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      flex-direction: column;
      padding:10px 0px;
      width: 50%;
      position: relative;
      img{
        width:90%;
        height: auto;
        box-shadow: 0px 0px 10px #000;
        z-index:900;
        
      }
      div{
        width:80%;
        height: 100%;
        background: white;
        color:#fff;
        font-size: .8em;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        background: linear-gradient(90deg, #000000 0%, #000000 0%, #FF0000 100%);
      }
      

    }
  }
  }
  @media screen and (max-width: 500px) {
     .wrapper {
    display: flex;
    flex-direction: row;
    
    flex-wrap: wrap;
  
    div {
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      flex-direction: column;
      padding:10px 0px;
      width: 100%;
      position: relative;
      img{
        width:90%;
        height: auto;
        box-shadow: 0px 0px 10px #000;
        z-index:900;
      }
      div{
        width:80%;
        height: 100%;
        background: white;
        color:#fff;
        font-size: .8em;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        background: linear-gradient(90deg, #000000 0%, #000000 0%, #FF0000 100%);
      }
      

    }
  }
  }
</style>