<template>
  <div>
    <input type="text" v-model="msg" @change="sendMsg" placeholder="なにか聞いてね！">
    <chat-button @click="sendMsg" v-bind:button-name = "buttonName"></chat-button>
  </div>
</template>

<script>
/* eslint-disable */
import chatButton from './chat-button.vue'
export default {
  components: {
    chatButton
  },
  data: function () {
    return {
      buttonName: 'send',
      msg: ''
    }
  },
  methods: {
    sendMsg: function () {
      //alert(this.msg+'sendingMessageが発火しました')
      this.$emit('sendingMessage', this.msg)
      this.msg = ''
    }
  }
}
</script>

<style>

</style>
