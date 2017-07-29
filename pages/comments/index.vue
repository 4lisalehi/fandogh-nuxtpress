<template>
  <div>
    <h2 class="subtitle">
      Comments
    </h2>
    <div class="comments">
      <comment-item v-for="comment in comments"
                    :key="comment.id"
                    :content="comment.content.rendered"
                    :author="comment.author_name"
                    :avatar="comment.author_avatar_urls[0]"
                    :date="comment.time_ago"></comment-item> 
    </div>
  </div>
</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import CommentItem from '~components/CommentItem'

Vue.component('comment-item', CommentItem)

export default {
  async asyncData ({params}) {
    let { data } = await axios.get(`https://wptavern.com/wp-json/wp/v2/comments`)
    return { comments: data }
  }
}

</script>

<style>

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

.comments {
  position: absolute;
  left: 60px;
  top: 240px;
}
</style>
