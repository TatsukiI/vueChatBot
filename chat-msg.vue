<template>
  <p>{{ msg }}</p>
</template>

<script>
export default {
  name: 'chat-msg',
  props: {
    msg: {
      type: String,
      required: true
    }
  }
}
</script>
