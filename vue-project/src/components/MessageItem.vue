<template>
    <div class="">
        <div class="mt-20">
            <b class="mr-4">Message {{ message.id }}:</b> 
            {{ message.message }}
            <my-button class="bg-transparent hover:bg-blue-500 text-blue-700 font-semibold hover:text-white py-2 px-4 border 
            border-blue-500 hover:border-transparent rounded mx-10 cursor-pointer text-center">Delete</my-button>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        message: {
            type: Object,
            required: true
        }
    }
}
</script>
<style>

</style>