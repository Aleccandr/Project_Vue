<template>
  <div>
    <form @submit.prevent>
    <input v-model="post.title"
           class="post"
           type="text"
           placeholder="Введите день">
      <input v-model="post.body"
             type="text"
             placeholder="Введите запись"
             class="post">
    <button class="btn"
            @click="createPost"> Добавить запись</button>
    </form>
  </div>
</template>
<script>
export default {
  data () {
    return {
      post: {
        id: '',
        title: ''
      }
    }
  },
  methods: {
    createPost () {
     this.post.id = Date.now();
      this.$emit('create', this.post);
      this.post = {
        title: ''

      }
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
  width: 90%;
  padding: 15px 15px;
  margin: 10px 10px;
  outline: none;
}
</style>