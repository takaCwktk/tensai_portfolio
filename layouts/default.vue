<template>
  <div>
    <nav class="navbar" role="navigation" aria-label="main navigation">
   <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <img src="png" width="112" height="28" >
      
    </a>
    

    <a role="button" class="navbar-burger burger" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
   </div>



  <div id="navbarBasicExample" class="navbar-menu">
    <div class="navbar-start">
      <nuxt-link :to="'/'"class="navbar-item">
        TOP
      </nuxt-link>

      <nuxt-link :to="'3dworks'" class="navbar-item">
        3Dworks
      </nuxt-link>
      <nuxt-link :to="'sketches'" class="navbar-item">
        Sketches
      </nuxt-link>

      <nuxt-link :to="'photodiary'" class="navbar-item">
        PhotoDiary
      </nuxt-link>

      <nuxt-link :to="'aboutme'" class="navbar-item">
        About Me
      </nuxt-link>

     </div>
   

    
  </div>
    </nav>
    <nuxt />
    <Footer />
  </div>
  
</template>

<script>
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Footer
  }
}
</script>



<style>
h1{
  margin-left:20px;
  padding:20px;
  font-size:3.5vw;
}

html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
