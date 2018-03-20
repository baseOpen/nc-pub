# NCForm



## 使用方法

```
import React, {Component} from 'react';
import ReactDOM from 'react-dom';
import { base } from 'nc-lightapp-front';
const { NCForm, NCFormControl } = base;
const NCFormItem = NCForm.NCFormItem;
class Demo1 extends Component {
    checkForm = (flag,obj) => {
        console.log(flag);
        console.log(obj);
    }
    render() {
        return (
            <NCForm  submitCallBack={this.checkForm}  >
                <NCFormItem  isRequire={true} labelName="姓名" htmlType="chinese" errorMessage="姓名格式错误" method="blur" >
                    <NCFormControl name="name" placeholder="只能输入中文"/>
                </NCFormItem>
                <NCFormItem isRequire={true} labelName="年龄" method="blur" reg={/^[0-9]+$/} errorMessage="年龄格式错误" >
                    <NCFormControl name="age"  />
                </NCFormItem>
            </NCForm>
        )
    }
}
export default Demo1;
```



## API

|参数|说明|类型|默认值|
|:---|:-----|:----|:------|
|submitCallBack|表单验证回调函数，参数两个，第一个为校验是否成功`true/false` 第二个为表单内元素数组`[{name: "", verify: false, value: ""}]`|function|-|
|useRow|是否使用栅格布局,如使用：需要再`FormItem`传格子数和label的格子数|bool|-|
|showSubmit|是否显示提交区域|bool|true|
|checkFormNow|是否立即校验，校验完成后将checkFormNow置为false，否则在form渲染的时候会直接校验|bool|false|


### FormItem 参数说明
|参数|说明|类型|默认值|
|:---|:-----|:----|:------|
|isRequire|是否必填|bool|false|
|errorMessage|错误提示信息，可传数组，和正则数组一一对应|node/array|"校验失败"|
|reg|校验正则，注：设置 `htmlType` 后 `reg` 无效；当不设置`isRequire`的时候，如果有值，会使用reg校验，如果值为空，则不校验；可传数组，和错误信息数组一一对应|regExp/array|-|
|method|何时校验 change/blur|string|-|
|inline|是否行内显示，须有`Form`才有效，单个`FormItem`无效|bool|false|
|labelName|输入框label标签内容|node|-|
|showMast|是否显示必输项的*|bool|false|
|asyncCheck|返回true则校验成功，false或无返回值则校验失败。参数为{name:xxx,value:xxx},如果使用asyncCheck，则其它校验props不生效|function|-|
|md|中等屏幕设备显示列数(≥992px)|number|-|
|labelMd|label中等屏幕设备显示列数(≥992px)|number|-|

### 自定义组件说明
- 需要有`onChange`方法，并且参数为改变后的值


### 其它说明
- `Form`的子元素中如果有`Button`并且此`Button`的`isSubmit=true`，则可以作为提交按钮
- `Form`整体校验时，会触发`FormItem`的校验
- `FormItem`的子元素，`name`必须存在且不能重复
- `FormItem`子元素只能存在一个
