<template>
  <div>
    <div v-cloak>1234</div>
    <div v-pre>{{ mes }}</div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      mes: '12341234',
      desc: 'v-pre：不进行编译',
    }
  },
}
</script>
<style scoped>
div[v-cloak] {
  display: none;
}
</style>
