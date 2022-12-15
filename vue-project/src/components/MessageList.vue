<template>
    <div>
        <div class="border-cyan-500 mx-auto" v-for="message in messages" v-bind:key="message.id">
          <div class="mt-20"><b class="mr-4">Message {{ message.id }}:</b> {{ message.message }}</div>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        messages: {
            type: Array,
            required: true
        }
    }
}
</script>
<style>

</style>