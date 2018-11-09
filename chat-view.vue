<template>
  <div>
    <chat-header @clearChatBody="clearChatLogs"></chat-header>
    <chat-timeline :chat-logs="chatLogs"></chat-timeline>
    <chat-form @sendingMessage="sendChat"></chat-form>
  </div>
</template>

<script>
/* eslint-disable */
import chatHeader from './chat-header.vue'
import chatTimeline from './chat-timeline.vue'
import chatForm from './chat-form.vue'
export default {
  components: {
    chatHeader,
    chatTimeline,
    chatForm
  },
  data: function () {
    return {
      chatLogs: []
    }
  },
  methods: {
    clearChatLogs: function () {
      if (confirm('チャットをリセットします。')) {
        this.chatLogs = []
      }
    },
    sendChat: function (arg) {
      this.chatLogs.push({id: this.chatLogs.length+1, me: true, msg: arg})
      this.chatLogs.push({id: this.chatLogs.length+1, me: false, msg: arg.split('').reverse().join('')})
    }
  }

}
</script>

<style>

</style>
