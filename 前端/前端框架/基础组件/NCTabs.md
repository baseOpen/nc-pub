# NCTabs

## 使用方法

```js
import React, {Component} from 'react';
import ReactDOM from 'react-dom';
import { base } from 'nc-lightapp-front';
const { NCTabs } = base;
const NCTabPane = NCTabs.NCTabPane;
class Demo1 extends Component {
    checkForm = (flag,obj) => {
        console.log(flag);
        console.log(obj);
    }
    render() {
        return (
            <NCTabs navtype="turn" contenttype="moveleft" defaultActiveKey="2">
            	<NCTabPane tab="Tab 1" key="1">测试测试 1</NCTabPane>
            	<NCTabPane tab="Tab 2" key="2">Content of Tab Pane 2</NCTabPane>
            	<NCTabPane tab="Tab 3" key="3">测试测试 3</NCTabPane>
            	<NCTabPane tab="Tab 4" key="4">Content of Tab Pane 4</NCTabPane>
            </NCTabs>
        )
    }
}
export default Demo1;
```



## API

### NCTabs

|参数|	说明|	类型|	默认值|
|---|---|---|---|
|activeKey|	设置当前激活的tabPanel的key|	String|	-|
|tabBarPosition|	tab头的定位，可以是['left','right','top','bottom']中选择|	String|	-|
|defaultActiveKey|	如果activeKey没有设置的时候，当初始化的时候设置当前激活的tabPanel的key|	String	|默认激活第一个|
|onChange	|tabPanel改变的时候的回调函数|	(key:string):void|	-|
|style|	添加到table上的style|	String|	u-tabs|
|onTabClick	tab 被点击的回调|	fun	|-|
|className	|在tab组件上添加className|	fun	|-|

### NCTabPane

|参数|	说明|	类型|	默认值|
|---|---|---|---|
|key|	对应 |activeKey	|string	|-|
|tab|	选项卡头显示文字|	string\	ReactNode|-|
|style|	选项卡样式|	Object|	-|