<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        دیجیاتو
      </h1>
      <h2 class="subtitle">
        آخرین نظرات کاربران
      </h2>
      <div class="comments">
        <div class="comment-div" v-for="comment in comments" v-bind:key="comment.id">
          <img v-bind:src="comment.author_avatar_urls" />
          <span class="user">کاربر: {{ comment.author }} </span>
          <span class="time">{{ comment.time_ago }}</span>
          <span class="content" v-html="comment.content.rendered"></span>
        </div>
      </div>

      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
        <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
        <nuxt-link class="button--green" to="/">Home</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>
import Logo from '~components/Logo.vue'
import axios from 'axios'

export default {
  layout: 'comments',
  components: {
    Logo
  },
  async asyncData ({params}) {
    let { data } = await axios.get(`http://digiato.com/wp-json/wp/v2/comments`)
    return { comments: data }
  }
}

</script>

<style>
.container{
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links{
  padding-top: 15px;
}

.links nuxt-link{
    margin-left: 15px;
}

.comments{
  direction: rtl;
  display: block;
}

.comment-div{
    display: block;
    width : 1100px;
    min-height: 220px;
    border-radius: 4px;
    padding: 10px 30px;
    margin-top: 70px;
    position: relative;
    text-align: right;
    box-shadow: 5px 5px 5px #888888;
}

.comment-div span{
    position: absolute;
}

.comment-div img{
  width: 90px;
  height: 90px;
  right: 15px;
  top: 15px;
  float: right;
  border: 1px solid grey;
  margin-top: auto;
  margin-bottom: auto;
}

.comment-div span.content{
    display: inline-block;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-size: 16px;
    right: 140px;
    width: 820px;
    direction: rtl;
    text-align: justify;
}

.comment-div span.user{
    top: 15;
    left: 15px;
}

.comment-div span.time{
    bottom: 15px;
    left: 15px;
}

</style>
