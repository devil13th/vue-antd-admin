<template>
  <div style="border:1px solid red;padding:16px;">
    Parent
    <attrs-child v-bind="d" :c="c" other-attr="otherAttr"></attrs-child>
  </div>
</template>
<script>
import AttrsChild from './AttrsChild'

export default {
  components: { AttrsChild },
  data: function() {
    return {
      d: {
        a: 1,
        b: 2,
      },
      c: 3,
      desc: '$attrs的使用',
    }
  },
}
</script>
<style scoped></style>
