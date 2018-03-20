## 文本输入框

> 分类： NC基础组件


### 简单示例

```
// 1.引入NCFormControl组件
import {base} from 'nc-lightapp-front';
const {NCFormControl}=base;

// 2.组件中引入NCFormControl（示例）
class Demo extends Component {
    constructor(props) {
        super(props);
        this.state = {
            value: "test"
        }
    }

    onChange = (e) => {
        this.setState({value: e});
    }
  render () {
    return (
      <div>
        <h1>文本输入框NCFormControl的使用实例</h1>
        <FormControl
            className="demo-input"
            value={this.state.value}
            onChange={this.onChange}
            size="sm"
        />
      </div>
    )
  }
}

```

### API

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|className|类名|string|''
|type|类型(text,search, submit,'checkbox'...)|string|'input'
|onChange|input值发生改变触发的回调|func|-
|onSearch|input type="search"前提下回车触发的回调 多用于搜索|func|-


