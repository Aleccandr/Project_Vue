<template>
  <div>
    <H1>Записная книжка</H1>
  </div>
  <FormL @create="createPost"/>
  <PostL :posts="posts"
          @remove="removePost"/>

</template>

<script>
import PostL from "@/components/PostL";
import FormL from "@/components/FormL"

export default {
  name: 'App',
  components: {
    PostL,
    FormL
  },
  data () {
    return {
      posts: [
        { id:1, title: 'Сегодня', body: 'Первая запись'},
        { id:2, title: 'Сегодня', body: 'Вторая запись'}
      ],
    }
  },
methods: {
    createPost (post) {
      this.posts.push(post);
    },
  removePost (post) {
      this.posts = this.posts.filter(p => p.id !== post.id)
  }
  }
}

</script>

<style>

</style>
