<template>
  <div>
      <chat-balloon
      v-for="chat in chatLogs"
      :key="chat.id"
      :isMe="chat.me"
      :message="chat.msg">
      </chat-balloon>
  </div>
</template>

<script>
/* eslint-disable */
import chatBalloon from './chat-balloon.vue'

export default {
  name: 'chat-timeline',
  components: {
    chatBalloon
  },
  props: {
    chatLogs: {
      type: Array,
      required: false
    }
  },
}
</script>

<style>

</style>
