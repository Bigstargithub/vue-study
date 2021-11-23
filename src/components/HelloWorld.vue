<template>
  <div>
  <h2 @click="$emit('click')">
    {{ msg }}
  </h2>
  <img
    src="~assets/logo.png"
    alt="HEROPY" />
  </div>
</template>

<script>
export default {
  props: {
    msg: { type: string }
  },
  emits: ['click']
}
</script>

<style scoped lang="scss">
  @import "~/scss/main";

  h2 {
    font-size:22px;
    color:$color--primary;
    & + img {
      width:120px;
    }
  }
</style>