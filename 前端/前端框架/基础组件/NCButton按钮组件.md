## 按钮

> 分类： NC基础组件


### 简单示例

```
// 1.引入NCButton组件
import {base} from 'nc-lightapp-front';
const {NCButton}=base;

// 2.组件中引入NCButton（示例）
class Demo extends Component {
    handleClick() {
            alert("谢谢你点我")
    }
    render () {
        return (
          <div>
            <h1>按钮NCButton的使用实例</h1>
            render() {
                return (
                    <NCButton shape="border" colors="primary" onClick={ this.handleClick }>事件按钮</NCButton>
                )
            }
          </div>
        )
    }
}

```

### API

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|size|按钮大小(lg xg sm)|string|-
|colors|颜色(primary/accent/success/info/warning/danger/default)|string|''
|shape|形状(block/round/squared/floating/pillRight/pillLeft/icon)|string	|''
|disabled|是否禁用(disabled 或 true false)|boolean|false
|bordered|是否是边框型(bordered 或 true false)	|boolean|false
|className|增加额外的class|string|''
|style|style 属性|object|''


