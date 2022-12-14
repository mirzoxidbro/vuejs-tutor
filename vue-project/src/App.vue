<template>
  <div>
    <div class="block p-6 rounded-lg shadow-lg bg-white max-w-sm">
        <form @submit.prevent>
          <div class="form-group mb-6">
            <label for="exampleInputEmail1" class="form-label inline-block mb-2 text-gray-700">message</label>
            <input @input="message = $event.target.value" :value="message" type="text" class="form-control block w-full px-3 py-1.5 text-base font-normal  text-gray-700  bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0
              focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" id="exampleInputEmail1"
              aria-describedby="emailHelp" placeholder="message">
          </div>
          <button @click="createMessage()" type="submit" class="px-6py-2.5 px-4 py-2 bg-blue-600 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-blue-700 hover:shadow-lg
                                  focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-blue-800 active:shadow-lgtransitionduration-150">Submit</button>
        </form>
      </div>
</div>
<div class="border-cyan-500 mx-auto" v-for="message in messages" v-bind:key="message.id">
  <div><b class="mr-4">Message {{ message.id }}:</b> {{ message.message }}</div>
</div>
</template>
<script>

export default {
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