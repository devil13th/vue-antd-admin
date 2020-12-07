<template>
  <div class="main">
    <div class="header">
      <h5>Header</h5>
      <slot name="headerSlot" :headerData="parentHeaderData"></slot>
    </div>

    <div class="content">
      <h5>Content</h5>
      <slot
        name="contentSlot"
        :contentData="parentContentData"
        :user="userInfo"
      ></slot>
    </div>

    <div class="footer">
      <h5>Footer</h5>
      <slot name="footerSlot" :footerData="parentFooterData"></slot>
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
      parentHeaderData: {
        title: 'This Is A Slot Example',
      },
      parentContentData: {
        title: 'Devil13th',
        content: "I'm A Student ,Nice To Meet You",
      },
      ParentfooterData: {
        copyRight: 'CopyRight ...',
      },
    }
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
