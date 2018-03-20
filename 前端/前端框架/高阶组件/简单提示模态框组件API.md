## 简单提示模态框组件API

```
//初始化
render(){
    const {modal } = this.props;
    let { createModal } = modal;
    
    return(
        <div>
             { createModal('modal') }
        </div>
    )
    
}

模态框显示  使用方法：
   props.modal.show('modal',{
                title:'确认取消',  //标题    
                content:'是否确认要取消？', //内容
                beSureBtnClick:() => {  //点击确认按钮事件
                    console.log('取消成功')


                }
            });


```

方法 | 参数说明
---|---
createModal(id) | id:模态框的id(string)
show(id,{ title, content, beSureBtnClick })| id:模态框的id(string)；<br>title:模态框的标题(string)；<br> content：显示内容(string)；<br> beSureBtnClick：确认按钮事件(function)


