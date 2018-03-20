## NCAffix 固钉

> 分类： NC基础组件


### 简单示例

```
// 1.引入NCAffix组件
import { base } from 'nc-lightapp-front';
const { NCAffix } = base;

// 2.组件中引入NCAffix（示例）
class Demo extends Component {
  render () {
    return (
      <div>
        <h1>NCAffix的使用实例</h1>
        <NCAffix
             offsetTop={200}
        >
          <div>NCAffix组件内容区域</div>
        </NCAffix>
      </div>
    )
  }
}

```

### API

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|offsetTop|固定被触发距离，默认是0 ，可选的属性|number|0|


