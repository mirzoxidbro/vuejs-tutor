<template>
  <label>
    <input :value="modelValue" @input="updateInput" >
  </label>
</template>
<script>
export default {
    name:"my-input",
    props: {
      modelValue: [String, Number],
    },
    methods: {
      updateInput(event){
        this.$emit('update:modelValue', event.target.value)
      }
    }
}
</script>
<style>

</style>