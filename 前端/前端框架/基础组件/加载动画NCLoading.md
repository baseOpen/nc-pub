# 加载动画  NCLoading

```
import { base } from 'nc-lightapp-front';
const { NCLoading } = base;

constructor(props) {
        super(props);
        this.state = {
            show: true
        }
    
    }

 render() {
        return (
            <div className="">
                <NCLoading
                    container={this}
                    show={this.state.show} >
                    加载中
                </NCLoading>
            </div>
        )
    }
```

参数 |  说明 | 类型 | 默认值
---|---|---|---
**container**| 渲染到的容器，通过this可以显示在该组件的上面  | this或者function | 默认显示在body上面
**show**|  控制loading显示/隐藏 | bool | true/false    
