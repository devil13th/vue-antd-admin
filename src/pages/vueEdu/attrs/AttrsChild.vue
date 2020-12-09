<template>
  <div style="border:1px solid green;padding:16px;">
    Child<br />
    a:{{ a }}<br />
    b:{{ b }}<br />
    c:{{ c }}<br />
    {{ $props }} (props中的属性)<br />
    {{ $attrs }}(不在props中的属性)<br />
    <a-button @click="showParent">console中显示$parent</a-button>
  </div>
</template>
<script>
export default {
  props: {
    a: {
      type: Number,
      default: 0,
    },
    b: {
      type: Number,
      default: 0,
    },
    c: {
      type: Number,
      default: 0,
    },
  },
  data: function() {
    return {}
  },
  methods: {
    showParent() {
      console.log(this.$parent)
    },
  },
}
</script>
<style scoped></style>
