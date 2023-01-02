<template>
            <div class="block p-6 rounded-lg shadow-lg bg-white max-w-sm">
              <form @submit.prevent>
                <div class="form-group mb-6">
                  <label for="exampleInputEmail1" class="form-label inline-block mb-2 text-gray-700">message</label>
                  <my-input v-model="message.message" type="text" class="form-control block w-full px-3 py-1.5 text-base font-normal  
                    text-gray-700  bg-white bg-clip-padding border border-solid border-gray-300 rounded transition ease-in-out m-0
                    focus:text-gray-700 focus:bg-white focus:border-blue-600 focus:outline-none" />
                </div>
                <my-button @click="createMessage()" type="submit" 
                  class="px-6py-2.5 px-4 py-2 bg-blue-600 text-white font-medium text-xs leading-tight uppercase rounded shadow-md 
                  hover:bg-blue-700 hover:shadow-lg focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-blue-800 
                    active:shadow-lgtransitionduration-150 cursor-pointer text-center">
                      Submit
                </my-button>
              </form>
        </div>

</template>
<script>
export default {
    data(){
        return {
            message: {
              message: ''
            }
        };
      },
    methods: {
      createMessage(){
            this.message.id = Date.now(),
            this.$emit('addMessage', this.message);
            this.message = {
              message: ''
            }
    }
  }
}
</script>
<style>

</style>