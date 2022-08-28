# obj-observer
js/ts 对象监听

1. 安装依赖
```shell
npm install obj-observer
# 或 npm i
```
2. 在需要的地方引入watch方法，监听对象或数组的变化
```javascript
import {watch} from 'obj-observer'
const [obj,dispose]=watch(
    {test:'hello world'},
    (value,oldValue)=>{
        console.log('trigger change',value,oldValue)
    })
obj.test='hi world' //'trigger change' {test:'hello world'} {test:'hi world'} 
```
