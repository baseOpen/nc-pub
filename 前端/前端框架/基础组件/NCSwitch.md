## NCSwitch

> 分类： NC基础组件


### 简单示例

```
隐藏代码
/**
 *
 * @title 默认开关
 * @description
 *
 */
import React, { Component } from "react";
import { base } from 'nc-lightapp-front';
const { NCSwitch } = base;
import { Icon,  Row, Col  } from 'tinper-bee';

class Demo1 extends Component {
  constructor(props) {
    super(props);
    this.state = {
      checked: true
    };
  }
  onChange = () => {
    this.setState({
      checked: !this.state.checked
    });
  };
  render() {
    return (
      <Row>
        <Col sm={2}>
          <NCSwitch />
        </Col>
        <Col sm={2}>
          <NCSwitch
            checked={this.state.checked}
            onChange={this.onChange}
          />
        </Col>
      </Row>
    );
  }
}



```

### API

NCSwitch

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|checked |指定当前是否选中 | Boolean |false|
|defaultChecked | 初始是否选中 | Boolean |false|
|onChange  |变化时回调函数,自定义参照demo |Function(checked:Boolean)| |
|disabled | 设置是否禁用 | Boolean| false|
|checkedChildren| 选中时的内容 | React |Node|
|unCheckedChildren| 非选中时的内容| React| Node|
|size  |大小设置，oneOf：primary,success,info,dark,warning  |string | ''|
|colors | 颜色设置，oneOf：sm, lg,''|  string | ''|


