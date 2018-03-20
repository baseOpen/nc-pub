## NCIcon 图标

> 分类： NC基础组件


### 简单示例

```js
// 1.引入NCIcon组件
import { base } from 'nc-lightapp-front';
const { NCIcon } = base;

// 2.组件中引入NCIcon（示例）
class Demo extends Component {
	render () {
		return (
			<div>
				<h1>NCIcon的使用实例</h1>
				<NCIcon type="uf-code" onClick={(e) => {
					console.log('图标')
				}}>
					<div>NCIcon组件内容区域</div>
				</NCIcon>
			</div>
		)
	}
}

```

### API

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|type|字体类名|string|-|


