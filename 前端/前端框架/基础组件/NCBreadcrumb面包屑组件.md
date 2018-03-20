## 面包屑

> 分类： NC基础组件


### 简单示例

```
// 1.引入NCBreadcrumb,NCBreadcrumbItem组件
import { base } from 'nc-lightapp-front';
const {NCBreadcrumb}=base;
const NCBreadcrumbItem=NCBreadcrumb.NCBreadcrumbItem;

// 2.组件中引入NCBreadcrumb,NCBreadcrumbItem（示例）
class Demo extends Component {
  render () {
    return (
      <div>
        <h1>面包屑NCBreadcrumb,NCBreadcrumbItem的使用实例</h1>
        <NCBreadcrumb>
            <NCBreadcrumbItem href="#">
		      Home
		    </NCBreadcrumbItem>
		    <NCBreadcrumbItem>
		      Library
		    </NCBreadcrumbItem>
		    <NCBreadcrumbItem active>
		      Data
		    </NCBreadcrumbItem>
        </NCBreadcrumb>
      </div>
    )
  }
}

```

### API

|参数|说明|类型|默认值|
|:--|:---:|:--:|---:|
|active|如果设置成true,渲染成span而不是a|bool|false
|href|给内部a标签设置的属性|string|''
|title|给内部a标签设置的属性|string|''


