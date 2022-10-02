<template>
 <div class="post" v-for="post in posts"
      v-bind:key="post.id"
      @remove="$emit('remove',post)">
   <div class="posts"> {{ post.title }}</div>
   <div class="posts"> {{ post.body }}</div>
   <div>
     <button class="" @click="$emit('remove', post)">Удалить</button>
   </div>
 </div>
</template>
<script>
 export default {
  props: {
    posts: {
      type: Array,
      required: true
    }
  }
 }
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
.post {
  width: 80%;
  padding: 15px 15px;
  margin: 10px 10px;
  border: 1px solid darkgrey;
  align-items: center;
  justify-content: space-between;
}
.posts {
  margin: 10px 0;
}
.btn {
  padding: 15px 15px;
  margin: 10px 10px;
  position: relative;
  right: 0;

}
</style>