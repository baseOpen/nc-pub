## NCDatePicker

> 分类： NC基础组件


### 简单示例

```

/**
 *
 * @title 选择日期
 * @description 以「日期」为基本单位，基础的日期选择控件
 */

import React, { Component } from "react";
// 1.NCDatePicker
import { base } from 'nc-lightapp-front';
const { NCDatePicker } = base;
import { Icon,  Row, Col  } from 'tinper-bee';

import zhCN from "rc-calendar/lib/locale/zh_CN";
import enUS from "rc-calendar/lib/locale/en_US";
import moment from "moment";

const format = "YYYY-MM-DD";

const dateInputPlaceholder = "选择日期";

function onSelect(d) {
  // console.log(d);
}

function onChange(d) {
  this.setState({
    value: d
  });
}

class Demo1 extends Component {
  constructor(props) {
    super(props);
    this.state = {
      value: moment()
    };
  }
  onChange = d => {
    console.log(d)
    
    this.setState({
      value: d
    });
  };
  render() {
    return (
      <div>
        <Row>
          <Col md={12}>
            <DatePicker
              format={format}
              onSelect={onSelect}
              onChange={this.onChange}
              locale={zhCN}
              defaultValue={this.state.value}
              placeholder={dateInputPlaceholder}
            />
          </Col>
        </Row>
      </div>
    );
  }
}

```

### API

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|format|日期格式|string|YYYY-MM-DD|
|prefixCls| 组件的前缀 |String | |
|className |添加节点的样式| String  ||
|style |添加内联样式 | Object  ||
|dateRender | 日期表格  |(current, value) => React.Node || 
|renderSidebar| 侧边栏 |() => React.Node  ||
|renderFooter  |扩展底边栏 |() => React.Node || 
|defaultValue | 默认值，输入框的默认值 |moment  ||
|value |日期 | moment  ||
|locale | 日历的语言| Object|  en_US|
|format | 日期格式化 |String  ||
|disabled | 是否禁用功能 | Boolean |false|
|disabledDate | 禁用的日期 |Function(current:moment):Boolean || 
|disabledTime  |禁用的时间| Function(current:moment):Object ||
|showDateInput |显示日期输入康| Boolean| true|
|showWeekNumber | 是否显示周数 | Boolean |false|
|showToday |是否显示今天 | Boolean| true|
|showOk  |底边栏是否显示ok按钮 |Boolean |auto|
|onSelect | 选择日期的回调函数| Function(date: moment) || 
|onChange | 日期改变的回调函数| Function(date: moment)  ||
|dateInputPlaceholder | 日期的placeholder | String  ||
|showTime | 是否显示时间选择面板|  Boolean ||
|renderIcon  |更改默认的图标 |Function  () =>||
