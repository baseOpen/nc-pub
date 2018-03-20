## NCMessage 气泡消息

> 分类： NC基础组件


### 简单示例

```
// 1.引入NCMessage
import { base } from 'nc-lightapp-front';
const { NCMessage } = base;

// 2.使用NCMessage（示例）
class Demo extends Component {
    construct(props){
        super(props)
    }

    success = () => {
        Message.create({content: 'This is a success message', color: 'success', position: 'bottom'});
    } 

    render () {
        return (
        <div>
            <Button
                colors="success"
                onClick={this.success}>
                success
            </Button>
        </div>
        )
    }
}

```

### API

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|content|气泡消息的内容|string/number|-|
|color|气泡颜色|dark/light/success/danger/warning/info/successlight/dangerlight/warninglight/infolight	'dark'|'dark'|
|position|气泡消息的位置|top/bottom/topRight/topLeft/bottomRight/bottomLeft|top|