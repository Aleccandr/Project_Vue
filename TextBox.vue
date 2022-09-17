<template>
  <div>
    <input type="text" :placeholder=this.placeholder>
  </div>
</template>
<script>
export default {
  name: "TextBox",
  props: {
    placeholder: {
      required: true,
      type: String
    },
  }
}
</script>
<style>

</style>