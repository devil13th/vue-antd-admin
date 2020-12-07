<template>
  <div style="border:1px solid pink;padding:8px;">
    <div style="padding:8px;">{{ str }}</div>
    <hr />
    slot-scope : {{ text }}
  </div>
</template>
<script>
export default {
  props: {
    text: {
      type: Object,
      default: function() {
        return {}
      },
    },
  },
  data: function() {
    return {
      str: "I'm A Slots",
    }
  },
}
</script>
<style scoped></style>
