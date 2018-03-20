## NCSelect 图标

> 分类： NC基础组件


### 简单示例

```js
// 1.引入NCSelect和NCOption组件
import { base } from 'nc-lightapp-front';
const { NCSelect } = base;
const NCOption = NCSelect.NCOption;

// 2.组件中引入NCSelect（示例）
class Demo extends Component {
	handleChange = value => {
		console.log(`selected ${value}`);
	};
	render () {
		return (
			<div>
				<h1>NCSelect的使用实例</h1>
				<NCSelect
					defaultValue="lucy"
					style={{ width: 200, marginRight: 6 }}
					onChange={this.handleChange}
				>
					<NCOption value="jack">boyuzhou</NCOption>
					<NCOption value="lucy">renhualiu</NCOption>
					<NCOption value="disabled" disabled>Disabled</NCOption>
					<NCOption value="yiminghe">yuzhao</NCOption>
				</NCSelect>
			</div>
		)
	}
}

```

### API

#### Select

|参数|说明|类型|默认值|
|---|----|---|------|
|value|指定当前选中的条目|string/array/react node|-|
|defaultValue|指定默认选中的条目|string/array/react node|-|
|onSelect|被选中时调用，参数为选中项的 value 值|func|-|
|onDeselect|取消选中时调用，参数为选中项的 option value 值，仅在 multiple 或 tags 模式下生效|func|-|
|onChange|选中 option，或 input 的 value 变化（combobox 模式下）时，调用此函数|bool|-|
|onSearch|文本框值变化时回调|func|-|
|onBlur|失去焦点的时回调|bool|-|
|onFocus|获得焦点时回调|func|-|
|placeholder|选择框默认文字	|string|-|
|disabled|是否禁用|bool|false|



#### Option

|参数|说明|类型|默认值|
|---|----|---|------|
|key|如果 react 需要你设置此项，此项值与 value 的值相同，然后可以省略 value 设置|string|-|
|value|默认根据此属性值进行筛选	|string|-|
|disabled|是否禁用|bool|false|


