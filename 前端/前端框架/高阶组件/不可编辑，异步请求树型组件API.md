
## 不可编辑，异步请求树型组件  API
```

  // 树节点 点击事件
    selectTree = (pk) => {
        console.log(pk)
    };


  // 树展开子节点事件，ajax请求子节点数据
    loadTreeData = (pk) => {
        this.queryTreeData(pk)
    };

    // 请求树 根节点—数据
    queryTreeData = (pk) => {
        let that = this;
        let data = {
            "pid":pk,
            "keyword":"",
            "pageInfo":{
                "pageIndex":0,
                "pageSize":10,
                "total":0,
                "totalPage":0
            },
            "queryCondition":{}
        };
        ajax({
            loading: true,
            url: '/ncdemo-web/bd/basedoc/regiontree.do',
            data: data,
            success: function (res) {
                if(res.success){
                    props.asyncTree.setTreeData('tree1', res.data.rows)//设置树组件数据
                }else {
                    alert(res.message)
                }
            },
            error: function (res) {
                alert(res.message)
            }
        });
    };
    render(){
        const {table, button, search, form, editTable, asyncTree, modal } = this.props;
        const { createAsyncTree } = asyncTree;
        return(
            <div>
                 { createAsyncTree({
                        treeId:'tree1',//树组件id
                        onSelect: this.selectTree.bind(this),//节点点击事件
                        loadTreeData: this.loadTreeData.bind(this),//节点展开事件
                    })}
            </div>
        )
    }
    
    
    
```

方法 | 参数描述/类型
---|---
createAsyncTree（{ treeId, onSelect, loadTreeData }）| treeId:组件id（string）<br> onSelect:节点点击事件(function)<br>  loadTreeData: 父节点展开事件（function）
setTreeData（treeId, data）| treeId:组件id（string）<br> data: 树型组件数据（array）


