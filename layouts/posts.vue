<template>
  <div>
    <div class="links">
      <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
      <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
      <nuxt-link class="button--green" to="/">Home</nuxt-link>
      <nuxt-link class="button--green" to="/posts">Posts</nuxt-link>
      <nuxt-link class="button--green" to="/comments">Comments</nuxt-link>
    </div>
    <nuxt/>
  </div>
</template>

<style scoped>
html
{
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*, *:before, *:after
{
  box-sizing: border-box;
  margin: 0;
}
.button--green
{
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}
.button--green:hover
{
  color: #fff;
  background-color: #3b8070;
}

.button--grey
{
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}
.button--grey:hover
{
  color: #fff;
  background-color: #35495e;
}

.posts{
  display: block;
}

.post-div{
    display: block;
    width : 1100px;
    min-height: 1800px;
    border-radius: 4px;
    padding: 10px 30px;
    margin-top: 70px;
    position: relative;
    text-align: left;
    box-shadow: 5px 5px 5px #888888;
}

.post-title{
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 24px;
}


.post-div img{
  width: 90px;
  height: 90px;
  right: 15px;
  top: 15px;
  float: left;
  border: 1px solid grey;
  margin-top: auto;
  margin-bottom: auto;
}

.post-div span.content{
    display: inline-block;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-size: 16px;
    left: 140px;
    width: 820px;
    text-align: justify;
}

.post-div span.time{
    bottom: 15px;
    left: 15px;
}

</style>
