<template>
  <div class="nav-bar">
    <ul class="root">
        <li>
        <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
        <nuxt-link to="/posts">Posts</nuxt-link>
        </li>
        <li>
        <nuxt-link to="/comments">Comments</nuxt-link>
        </li>
        <li>
        <nuxt-link to="/categories">Categories</nuxt-link>
        </li>
        <li>
        <nuxt-link to="/users">People</nuxt-link>
        </li>
    </ul>
  </div>
</template>

<script>

export default {
  data: function () {
    return {}
  }
}

</script>

<style scoped>

.nav-bar > ul{
  list-style: none;
  margin-top: 120px;
  margin-left: 10px;
}

.nav-bar > ul > li{
  width: 250px;
  float: left;
  background-color: #35495e; 
}

.nav-bar > ul > li > a{
  color: azure;
  display: block;
  text-align: center;
  width: 200px;
  line-height: 40px;
  font-size: 14px;
  padding: 0 20px;
  border: 1px solid #35495e;
  text-decoration: none;
}

.nav-bar > ul > li > a:hover{
  background-color: black;
}

</style>
