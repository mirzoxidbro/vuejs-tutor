<template>
    <div>
        <div
            class="border-cyan-500 mx-auto" border="1"
            v-for="message in xabarlar" 
            v-bind:key="message.id">
            <message-item :message="message" />
        </div>
    </div>
</template>
<script>
import MessageItem from './MessageItem.vue'
export default {
    components:{
        MessageItem
    },
    props: {
        xabarlar: {
            type: Array,
            required: true
        }
    }
}
</script>
<style>

</style>