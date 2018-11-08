<template>
  <button @click="clickHandle">{{buttonName}}</button>
</template>

<script>
  export default{
    name: 'chat-button',
    props: {
      buttonName: {
        type: String,
        required: true
      }
    },
    methods: {
      clickHandle: function () {
        this.$emit('click')
      }
    }
  }
</script>