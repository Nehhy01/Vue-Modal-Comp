<template>
    <input type="text" ref="name" :placeholder="placeholder">
    <button type="button" @click="handleClick" >Submit</button>
 </template>

 <script>
export default {
    props: [
        'placeholder'
    ],
    methods: {
        handleClick() {
            this.$refs.name.focus()
        }
    }}


</script>

 <style>
 </style>