<template>
  <img v-bind:src="selectIconUrl">
</template>

<script>
const myUrl = "https://img.icons8.com/ios/50/000000/user-male.png"
const yourUrl = "https://img.icons8.com/dotty/50/000000/bot.png"

export default {
  name: 'chat-icon',
  props: {
    iconType :{
      type: Boolean,
      require: true,
    }
  },
  computed: {
    selectIconUrl: function () {
      if (this.iconType) {
        return myUrl
      } else {
        return yourUrl
      }
    }
  }
}
</script>
