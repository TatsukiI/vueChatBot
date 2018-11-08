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
  data: function () {
    return {
      chatLogs: [
        {id: 1, me: true, msg: 'hello chatbot!'},
        {id: 2, me: false, msg: 'hello human!'}
      ]
    }
  }
}
</script>

<style>

</style>
