<template>
  <table>
    <tr>
      <td>{{ headerTitle }}</td>
      <td><chat-button @click="clearChatBody" v-bind:button-name="buttonName"></chat-button></td>
    </tr>
  </table>
</template>

<script>
/* eslint-disable */
import chatButton from './chat-button.vue'

export default {
  name: 'chat-header',
  components: {
    chatButton
  },
  data: function () {
    return {
      buttonName: 'Upd',
      headerTitle: 'TEST'
    }
  },
  methods: {
    clearChatBody: function () {
      //salert('clearChatBodyが発火しました')
      this.$emit('clearChatBody')
    }
  }

}
</script>


