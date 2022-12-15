<template>
    <div>
        <div class="border-cyan-500 mx-auto" v-for="message in xabarlar" v-bind:key="message.id">
          <div class="mt-20"><b class="mr-4">Message {{ message.id }}:</b> {{ message.message }}</div>
        </div>
    </div>
</template>
<script>
export default {
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