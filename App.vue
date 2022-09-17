<template>
<Todo></Todo>
<TextBox></TextBox>
<ChekList></ChekList>

</template>

<script>
import Todo from "@/Todo";
import ChekList from "@/components/ChekList"
import TextBox from "@/components/TextBox"
export default {
  components: {
    Todo,
    ChekList,
    TextBox
  }
}
</script>

<style>
* {
  margin-bottom: 10px;
}
</style>
