<template>
  <div>
    <button @click="addlike">Like</button>
    <button @click="adddislikes">Dislikes</button>
    <div>
      Like! {{ likes}}
    </div>
    <div>
      DisLike! {{ dislikes}}
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return{
      likes:0,
      dislikes:0,
    }
  },
  methods: {
    addlike(){
      this.likes +=1;
    },
    adddislikes () {
      this.dislikes +=1;
    }
  }
}

</script>
<style>


</style>