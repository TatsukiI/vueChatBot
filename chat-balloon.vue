<template>
  <div>
    <chat-icon :icon-type="this.isMe"></chat-icon>
    <chat-msg :msg="this.message"></chat-msg>
  </div>
</template>

<script>
/* eslint-disable */
import chatIcon from './chat-icon.vue'
import chatMsg from './chat-msg.vue'

export default {
  name: 'chat-balloon',
  components:{
    chatIcon,
    chatMsg
  },
  props:{
    isMe: {
      type: Boolean,
      //TODO
      required: false,
      default: true
    },
    message: {
      type: String,
      required: false,
      default: 'hello chat bot'
    }
  },
}
</script>

<style>

</style>
