<script>
export default {
  name: 'item',
  props: {
    id: {
      type: Number,
      default: 1,
    },
  },
  render() {
    const hText = `
                       <h${this.id} style="background:red;">${this.$slots.default[0].text}</h${this.id}>
                     `
    return <div domPropsInnerHTML={hText}></div>
  },
}
</script>
