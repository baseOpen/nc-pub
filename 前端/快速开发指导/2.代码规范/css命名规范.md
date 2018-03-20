# css命名规范

命名规范遵循两个原则：
1. 不影响其他页面的样式。
2. id、class名语义化

## 页面级css命名规范

- 页面的最外层元素需要有id属性，命名规范是：领域名-模块名-节点名

```stylesheet
/*index.less*/
/*领域-模块-节点*/
#field-module-node {}
```

- class选择器要写在id选择器下面，防止与其他样式冲突
- 页面区域命名

```stylesheet
/*index.less*/
#field-module-node {
    /*头部*/
    .header {} 
    /*导航区*/
    .nav {} 
    /*菜单区*/
    .menu {} 
    /*页面主体*/
    .content {} 
    /*底部*/
    .footer {} 
}
```

- 页面区域下的子元素的class命名尽量语义化，最好带有业务含义

```stylesheet
/*index.less*/
#field-module-node {
    .header {
        /*查询区*/
        .search-area {}
    } 
    .nav {} 
    .menu {} 
    .content {
        /*表单区*/
        .form-area {}
        
        /*表格区*/
        .table-area {}
        
        /*侧拉框*/
        .side-slide {}
        
        /*左侧侧拉框*/
        .side-slide-left {}
        
        /*右侧侧拉框*/
        .side-slide-right {}
        
        
        /*全屏侧拉框*/
        .side-slide-full {}
        
        /*消息提示弹窗*/
        .msg-modal {}
        
        /*确认提示弹窗*/
        .confirm-modal {}
        
        /*变更记录弹窗*/
        .modify-modal {}
        
        /*图片上传 + 预览*/
        .img-uploader {
        
            /*主预览框*/
            .main-preview {}
            
            /*次预览框*/
            .secondary-preview {}
        }
    } 
    .footer {} 
}
```

## 组件级css命名规范
- 与页面级css规范基本一致，只是最外层元素没有id属性，而是要有**以组件特性命名**的class属性，如果是领域特有的组件，在class前加上领域名（领域名-class）



