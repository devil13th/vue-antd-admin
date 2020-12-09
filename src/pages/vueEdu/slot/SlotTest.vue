<template>
  <div class="body">
    <h1>插槽 Slot 的使用</h1>

    <slot-test-parent>
      <template v-slot:headerSlot="slotProps" ref="headerRef">
        <slot-test-child :text="slotProps"></slot-test-child>
      </template>
      <template v-slot:contentSlot="slotProps">
        <slot-test-child :text="slotProps" :cb="showFn"></slot-test-child>
      </template>
      <!-- v-slot 也可以用 # 符号代替 -->
      <template v-slot:footerSlot="slotProps">
        <slot-test-child
          :text="slotProps"
          :cb="slotProps.cb"
          ref="footerRef"
        ></slot-test-child>
      </template>
    </slot-test-parent>
    <a-button @click="showSlots" type="primary"
      >show this.$slots console</a-button
    >
  </div>
</template>
<script>
import SlotTestChild from './SlotTestChild.vue'
import SlotTestParent from './SlotTestParent'
export default {
  components: {
    SlotTestParent,
    SlotTestChild,
  },
  data: function() {
    return {
      a: 1,
      b: 2,
    }
  },
  methods: {
    showSlots() {
      console.log(this.$children)
    },
    showFn() {
      alert('HAHA')
    },
  },
  computed: {
    desc() {
      return 'Solt 和 Scoped 的使用'
    },
  },
}
</script>
<style scoped>
.body {
  background: #fff;
  padding: 16px;
}
</style>
