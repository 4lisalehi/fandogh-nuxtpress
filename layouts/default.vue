<template>
  <div>
    <logo/>
    <nav-bar></nav-bar>
    <section class="container">
      <div>
        <nuxt/>
      </div>
    </section>
  </div>
</template>

<script>
import Vue from 'vue'
import Logo from '~components/TavernLogo'
import NavBar from '~components/NavBar'
import Footer from '~components/Footer'

Vue.component('nav-bar', NavBar)
Vue.component('footer-bar', Footer)

export default {
  components: {
    Logo
  }
}
</script>

<style>
html{
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after{
  box-sizing: border-box;
  margin: 0;
}

.title{
  position: absolute;
  top: 120px;
  left: 0;
}

.subtitle{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
  position: absolute;
  left: 50px;
  top: 170px;
}

.button--green{
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover{
  color: #fff;
  background-color: #3b8070;
}

.button--grey{
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover{
  color: #fff;
  background-color: #35495e;
}

.container{
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.posts{
  position: absolute;
  left: 120px;
  top: 230px;
}

</style>
