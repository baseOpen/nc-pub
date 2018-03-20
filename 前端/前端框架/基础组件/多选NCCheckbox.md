# 多选 NCCheckbox

```
import React, { Component } from 'react';
import { base } from 'nc-lightapp-front'
const { NCCheckbox } = base;

class Demo2 extends Component {
    constructor(props) {
		super(props);
		this.state = {
			checked: false
		}
	}
	changeCheck=()=> {
		this.setState({checked:!this.state.checked});
	}
	render(){
		return (
			<div className="demo-checkbox">
				<NCCheckbox colors="info" 
				disabled 
				onChange={this.changeCheck}
				checked={this.state.checked}
				>checkbox</NCCheckbox>
		    	<NCCheckbox defaultChecked={this.state.checked}>checkbox2</NCCheckbox>
			</div>
		)
	}
}


```
参数 |  说明 | 类型 | 默认值
---|---|---|---
**disabled**| 是否可用 | bool | false
**onChange**|  监听改变| fun |   
**defaultChecked**|  默认是否选中| bool |  false
**checked**| 是否选中| bool |  


