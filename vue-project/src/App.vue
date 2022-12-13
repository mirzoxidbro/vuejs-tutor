<template>
<div class="border-cyan-500 m-10" v-for="message in messages" v-bind:key="message.id">
  <div><b class="mr-4">Message {{ message.id }}:</b> {{ message.message }}</div>
</div>
</template>
<script>
import { defineSSRCustomElement } from 'vue';

export default {
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
      increment(){
        this.count++
      },
      decrement(){
        this.count--
      }
    },
}
</script>
<style>

</style>