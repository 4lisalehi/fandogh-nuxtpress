<template>
  <div class="post-div">
      <span class="post-title" v-html="title"></span>
      <span class="content" v-html="content"></span>
      <span class="time">{{ date }}</span>
  </div>
</template>

<script>

export default {
  props: ['title', 'date', 'content']
}
</script>

<style scoped>

.post-div{
  padding: 20px 20px 20px 20px;
  text-align: left;
  display: block;
  width: 1200px;
  height: fit-content;
  box-shadow: 5px 5px 5px #888888;
  margin-top: 30px;
  border: 1px solid #888888;
}

.post-title {
  font-weight: bold;
}

.time {
  float: right;
}

</style>
