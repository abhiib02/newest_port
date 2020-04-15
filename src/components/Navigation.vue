<template>
<div>
  <nav>
    <a class="brand" href="/"><img src="../assets/imgs/logo.svg" alt=""></a>
    <ul>
      <li>
        <router-link to="/">
          <i class="fas fa-home"></i>Home
        </router-link>
      </li>
      <li>
        <router-link to="/about">
          <i class="fas fa-user"></i>About
        </router-link>
      </li>
      <li>
        <router-link to="/skills">
          <i class="fas fa-keyboard"></i>Skills
        </router-link>
      </li>
      <li>
        <router-link to="/work">
          <i class="fas fa-pencil-ruler"></i>Work</router-link>
      </li>
      <li>
        <router-link to="/contact">
          <i class="far fa-envelope"></i>Contact</router-link>
      </li>
    </ul>
    <!--<ul id="social" class="">
            <li><a href="https://www.linkedin.com/in/abhishek-bhardwaj-191b9784/" target="_blank" rel="noopener noreferrer"><i class="fab fa-linkedin"></i></a></li>
            <li><a href="https://dynamohack.blogspot.com/" target="_blank" rel="noopener noreferrer"><i class="fab fa-blogger"></i></a></li>
            <li><a href="https://www.instagram.com/abhiib02/" target="_blank" rel="noopener noreferrer"><i class="fab fa-instagram"></i></a></li>
            <li><a href="https://codepen.io/abhishek-bhardwaj/" target="_blank" rel="noopener noreferrer"><i class="fab fa-codepen"></i></a></li>
        </ul>-->
         <div></div>
  </nav>
 
</div>
</template>
<style lang="scss" scoped>

nav{
  width:70px;
  height: 100vh;
  background: black;
  position: fixed;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  z-index: 1000;
  a{
    img{
      padding:5px;
    }
  }
}

ul{
  margin:0;
  padding:0;
  text-align: center;
  li{
    margin:30px 0px;
    a{
      color:#fff;
      text-decoration: none;
    }
  }
}
@media screen and (max-width: 700px) {

    nav{
    width:100%;
    height: 60px;
    background: black;
    position: fixed;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    z-index: 1000;
    a{
      img{
        position: fixed;
        height:50px;
      }
    }
  }

  ul{
    margin:0;
    padding:0;
    text-align: center;
    z-index: 1000;
    li{
      display: inline;
      margin:2px;
      font-size: .8rem;
      a{
        color:#fff;
        text-decoration: none;
      }
    }
  }

}
</style>