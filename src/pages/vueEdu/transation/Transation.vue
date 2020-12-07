<template>
  <div>
    [{{ show }}]
    <a-button type="primary" @click="toggle"> Toggle </a-button>
    <transition name="fade">
      <div v-if="show" class="x" :key="`dxa1`">1234</div>
      <div v-if="!show" class="x" :key="`dxa2`">4321</div>
    </transition>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      show: true,
      desc: 'Transition 动画的使用',
    }
  },
  methods: {
    toggle() {
      this.show = !this.show
    },
  },
}
</script>
<style>
.fade-enter-active,
.fade-leave-active {
  transition: all 1s ease;
}
.fade-enter,
.fade-leave-to {
  width: 0px !important;
  height: 0px !important;
  transform: translateX(-20px);
}
.fade-enter-to,
.fade-leave {
  width: 100% !important;

  height: 200px !important;
  transform: translateX(0px);
  overflow: hidden;
}

.x {
  width: 100%;
  height: 200px;
  overflow: hidden;
  border: 1px solid red;
}
</style>
