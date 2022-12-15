<template>
  <div class="ml-5">
      <post-form/>
      <message-list v-bind:messages="messages"/>
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
        ],
        message: ""
      }
    },
    methods: {
      createMessage(){
        const newMessage = {
          id: Date.now(),
          message: this.message
        }
        this.messages.push(newMessage)

        this.message = ''
      }
    },
}
</script>
<style>

</style>