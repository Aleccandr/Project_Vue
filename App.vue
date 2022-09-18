<template>
 <TabColor></TabColor>
 <div class="page">
 
 <button сlass="show-modal-button" @click="showModal">Показать модальное окно</button>

 <modal-window ref="modal"></modal-window>
 
</div>
</template>
<script>
import TabColor from "@/components/TabColor.vue"
import ModalWindow from "./components/ModalWindow.vue";


export default {
  name: 'App',
  components: {
    TabColor,
    ModalWindow
},
methods: {
  showModal: () => {
    this.$refs.modal.show = true
  }
},
}
  
</script>

<style>
</style>