<template>
  <div class="dark">
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
    .dark{
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        min-height: 100%;
        padding: 10px;
        color: white;
        background: black;
    }
    .dark a{
        color: green;
    }
    .dark a:hover{
        color: yellow;
    }
</style>
