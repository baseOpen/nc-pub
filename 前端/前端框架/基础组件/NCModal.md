# NCModal

## 使用方法

```js
import React, {Component} from 'react';
import ReactDOM from 'react-dom';
import { base } from 'nc-lightapp-front';
const { NCModal } = base

class ModalDemo extends Component {
    constructor(props) {
        super(props);
        this.state = {
            showModal: false
        };
        this.close = this.close.bind(this);
        this.open = this.open.bind(this);
    }

    close() {
        this.setState({ showModal: false });
    }

    open() {
        this.setState({ showModal: true });
    }
    render () {
        return (
            <div>
              <Button color="primary" size="large" onClick={this.open}>
                点击打开模态框
              </Button>
              <NCModal show = {
                  this.state.showModal
              }
              onHide = {
                  this.close
              }>
                <NCModal.Header>
                  <NCModal.Title>标题</Modal.Title>
                </NCModal.Header>

                <NCModal.Body>
                  正文描述。。。
                </NCModal.Body>

                <NCModal.Footer>
                  <Button>关闭</Button>
                  <Button color="primary">确认</Button>
                </NCModal.Footer>

              </NCModal>
            </div>
        )
    }
}

);

ReactDOM.render(
        <ModalDemo />
        , document.getElementById('target'));
```

## API

NCModal

|参数|说明|类型|默认值|
|:---|:-----|:----|:------|
|backdrop|是否弹出遮罩层/遮罩层点击是否触发关闭|boolean/"static"|true|
|show|是否打开模态框|string|-|
|dialogClassName|传递给模态框的样式| class |-|
|onHide|关闭时的钩子函数|function|-|
|size|模态框尺寸|sm/lg/xlg|-|
|onEnter|开始显示时的钩子函数|function|-|
|onEntering|显示时的钩子函数|function|-|
|onEntered|显示完成后的钩子函数|function|-|
|onExit|隐藏开始时的钩子函数|function|-|
|onExiting|隐藏进行时的钩子函数|function|-|
|onExited|隐藏结束时的钩子函数|function|-|
|onShow|当模态框显示时的钩子函数|function|-|

NCModal.Header

|参数|说明|类型|默认值|
|:---|:-----|:----|:------|
|closeButton|是否显示关闭按钮|boolean|false|

