## NCRadio

> 分类： NC基础组件


### 简单示例

```

/**
 *
 * @title NCRadio
 * @description `colors`参数控制背景色
 */

import React, { Component } from 'react'
import { base }  from 'nc-lightapp-front';
const { NCRadio } = base;



class Demo1 extends Component{
  constructor(props) {
    super(props);
    this.state = {
      selectedValue: 'apple'
    };
  }
  handleChange(value) {
    this.setState({selectedValue: value});
  }
  render() {
    return (
      <NCRadio.NCRadioGroup
        name="fruit"
        selectedValue={this.state.selectedValue}
        onChange={this.handleChange.bind(this)}>

          <NCRadio value="apple" >apple</NCRadio>

          <NCRadio value="orange" >Orange</NCRadio>

          <NCRadio disabled value="watermelon" >Watermelon</NCRadio>

      </NCRadio.NCRadioGroup>
    )
  }
};


```

### API


Radio

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|color |one of: primary/success/info/error/warning/dark |string | |
|disabled | 是否可用 | bool  |false|
|style |添加style| object | {}|
|className |传入列的classname |String  ||


RadioGroup

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|onChange | 暴露在外层的触发radio是否选中的方法 | func | |
|selectedValue |被选中的radio值|  string | |
|name  |radio组名 |string | ''|
|Children | Radio子组件 | obj | |
