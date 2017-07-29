<template>
  <div>
    <h2 class="subtitle">
      Posts
    </h2>
    <div class="posts">
      <post-item v-for="post in posts"
              :key="post.id" 
              :title="post.title.rendered" 
              :date="post.date" 
              :content="post.content.rendered"></post-item>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import PostItem from '~components/PostItem'

Vue.component('post-item', PostItem)

export default {
  async asyncData ({params}) {
    let { data } = await axios.get(`https://wptavern.com/wp-json/wp/v2/posts`)
    return { posts: data }
  }
}

</script>

<style>

.posts {
  position: absolute;
  left: 60px;
  top: 240px;
}

</style>
