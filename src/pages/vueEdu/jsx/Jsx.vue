<script>
import JsxChild from './JsxChild'
import { Button, Input } from 'ant-design-vue'

export default {
  name: 'item',
  props: {
    id: {
      type: Number,
      default: 1,
    },
  },
  data: function() {
    return {
      name: 'devil13th',
      a: 'x',
    }
  },
  methods: {
    showName() {
      alert(`My Name Is ${this.name}`)
    },
  },
  render() {
    const myDom = <div style="background:green;">1234</div>
    const hText = `xxxxxxxx`
    return (
      <div>
        12341234
        <JsxChild id={1} onClick={this.showName}>
          {hText}
        </JsxChild>
        <Button onClick={this.showName} type="primary">
          xxx
        </Button>
        {this.a}
        <Input></Input>[{myDom}]
      </div>
    )
  },
}
</script>
