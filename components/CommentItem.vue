<template>
  <div class="comment-div">
    <img :src="avatar" />
    <span class="user">{{ author }}</span>
    <span class="time">{{ date }}</span>
    <span class="content" v-html="content"></span>
  </div>
</template>

<script>

export default {
  props: ['avatar', 'author', 'date', 'content']
}

</script>

<style scoped>

.comment-div{
  padding: 20px 20px 20px;
  text-align: left;
  display: block;
  width: 1200px;
  height: fit-content;
  box-shadow: 5px 5px 5px #888888;
  margin-top: 30px;
  border: 1px solid #888888;
}

.user{
  font-weight: bold;
}

</style>
