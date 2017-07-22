<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        Wptavern
      </h1>
      <h2 class="subtitle">
        Comments
      </h2>
      <div class="comments">
        <div class="comment-div" v-for="comment in comments" v-bind:key="comment.id">
          <img v-bind:src="comment.author_avatar_urls[0]" />
          <span class="user">{{ comment.author_name }}</span>
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
    let { data } = await axios.get(`https://wptavern.com/wp-json/wp/v2/comments`)
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
</style>
