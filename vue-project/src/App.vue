<template>
  <div class="ml-5">
      <post-form @addMessage="createMessage"/>
      <message-list :xabarlar="messages"/>
  </div>
</template>
<script>
import PostForm from './components/PostForm.vue'
import MessageList from './components/MessageList.vue'
export default {
  components: {
    PostForm,
    MessageList
  },
    data(){
      return {
        messages: [
          {id:1, message: "xabar 1"},
          {id:2, message: "xabar 2"},
          {id:3, message: "xabar 3"},
        ]
      }
    },
    methods: {
      createMessage(message){
        this.messages.push(message)
      }
    },
}
</script>
<style>

</style>