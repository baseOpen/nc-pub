# 分页器 NCPagination

```
import { base } from 'nc-lightapp-front';
const { NCPagination } = base;
class Demo3 extends Component {
constructor(props) {
		super(props);
		this.state = {
			activePage:1
		}
	}
handleSelect(eventKey) {
	    this.setState({
	      activePage: eventKey
	    });
	}
render() {
	    return (
	      <div>
	        <NCPagination
	        	first
	        	last
	        	prev
	        	next
	        	boundaryLinks
		        items={20}
		        maxButtons={5}
		        activePage={this.state.activePage}
		        onSelect={this.handleSelect.bind(this)} />
	      </div>
	    );
	}
	}
	
```


参数 |  说明 | 类型 | 默认值
---|---|---|---
**first**|  显示第一页按钮  | bool | false
**last**|  显示最后一页按钮  | bool | last    
**prev**|  显示上一页按钮  | bool | false 
**next**|  显示下一页按钮  | bool | false
**boundaryLinks**|  显示边界按钮  | bool | false
**items**|  总页数 | number | ''
**maxButtons**|  显示最多页数按钮 | number | ''
**activePage**| 哪一页是激活状态 | number | ''
**onSelect**| 切换页的方法 | func | ''