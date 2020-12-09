<template>
  <div class="main">
    <div class="header">
      <h5>Header</h5>
      <slot name="headerSlot" :headerData="a"></slot>
    </div>

    <div class="content">
      <h5>Content</h5>

      <slot name="contentSlot" :contentData="b" :user="userInfo"></slot>
    </div>

    <div class="footer">
      <h5>Footer</h5>
      <slot name="footerSlot" :footerData="parentFooterData" :cb="cb"></slot>
    </div>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      str: "I'm A Parents",
      userInfo: {
        firstName: 'thd',
        lastName: 'devil13ths',
      },
      a: {
        title: 'This Is A Slot Example',
      },
      b: {
        title: 'Devil13th',
        content: "I'm A Student ,Nice To Meet You",
      },
      parentFooterData: {
        copyRight: 'CopyRight ...',
      },
    }
  },
  methods: {
    cb: function(x) {
      alert(
        "I'm a callback function:" + this.parentFooterData.copyRight + ',' + x
      )
    },
  },
}
</script>
<style scoped>
.main {
  height: 100%;
  border: 1px solid red;
}
.header {
  margin: 8px;
  border: 1px solid red;
}
.content {
  margin: 8px;
  border: 1px solid yellow;
}
.footer {
  margin: 8px;
  border: 1px solid green;
}
</style>
