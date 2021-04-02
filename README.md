# public-layer
**这是一个基于 vue 的动态弹框插件**
**它对标的是layer.js,和layer不同的是：**
**1.它零依赖不需要Jquery支持**
**2.它支持vue,却不限于vue**
**3.它是函数式的调用方式**
**4.它的样式支持自定义**
**4.它的行为支持自定义**
****

# 功能项
**支持拖拽**
**支持多弹框**
**支持最大化、最小化**
**支持自定义皮肤**
**支持mixin混淆，用于个性化定制弹框**
**支持...更多支持详见配置项**
****

# 能做什么？
**配合UI实现不规则弹框**
**配合UI实现超炫酷弹框**
**配合业务需要同时造出n个弹框...**
****
# 安装
npm install vue-pubilc-layer -s
****
# 修改vue.config.js配置，runtimeCompiler：true
```javascript
module.exports = {
    runtimeCompiler: true
    .....//其余自己的配置
}
```
****
# main.js引入
```javascript
import layer from 'vue-pubilc-layer'
Vue.use(layer,option);
//option 详细信息见文档后面
```
****
## 使用示例

```javascript
vm.$layer.open(option);
option 详细信息见文档后面
```
****
### 静态方法

open(option) //打开弹框,并且返回弹框实例

close(instance) //关闭弹框

closeAll() //关闭所有弹框
****
### option 参数选项

###
{
###
hasHead: true, //是否拥有头部
###
customHead: null, //自定义头部（支持组件、html代码片段、dom元素）
###
title: "测试", //标题
###
hasMin: false, //是否有最小化按钮
###
hasMax: false, //是否有最大化按钮
###
content: null, //弹框内容（支持组件、html代码片段、dom元素）
###
move: true, //是否可以拖动
###
shade: true, //是否有遮罩
###
minWidth: 300, //最小化宽度
###
minHight: 40, //最小化高度
###
bottomOff: 30, //最小化后距离窗口底部距离
###
leftOff: 4, //最小化后距离窗口左边距离
###
rowGap: 8, //行间距
###
colGap: 8, //列间距
###
location: {
###
//弹框位置，可由对象指定,为空则默认居中显示，左上角和右下角二选一，支持px和百分比
###
top: null,
###
left: null,
###
bottom: "10%",
###
right: "10px",
},
###
area: {
###
//弹框大小，支持px和百分比
###
height: "300px",
###
width: "30%",
###
},
###
subData: null, //用于弹框接受参数
###
multiple: false, //是否为多弹框模式
###
blank: false, //是否在点击空白处自动关闭弹框，仅在 shade 为 true 时有效
###
mixin: null, //混淆，用于完全个性化定制
###
theme: null, //自定义皮肤
###
//回调开始
###
success: null, //弹出成功后回调 type: Function
###
cancel: null, //弹框关闭回调，type: Function
###
minBack: null, //最小化回调 type: Function
###
maxBack: null, //最大化回调 type: Function
###
restore: null, //复原后回调 type: Function
};
****
### 实例方法

```javascript
close() //关闭当前弹框
min() //最小化当前弹框
max() //最大化当前弹框
reset() //窗口复原
....
```
****
### 效果图
![回调函数演示](https://img-blog.csdnimg.cn/20210402234803754.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzI3NTMyMTY3,size_16,color_FFFFFF,t_70#pic_center)
![多弹框测试](https://img-blog.csdnimg.cn/20210402235134408.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzI3NTMyMTY3,size_16,color_FFFFFF,t_70#pic_center)

### 扩展
**重要的事情说三遍**
**重要的事情说三遍**
**重要的事情说三遍**
###
其中 mixin 参数可搭配自定义组件实现和自定义主题实现完全个人化制定弹框
**如果不了解vue的mixin的用法，可以先查看[官方文档](https://cn.vuejs.org/v2/api/#Vue-mixin)**
###
初始化 Vue.use(layer,option); 其中 option 可以设置全局弹框的配置项，
如个别弹框有特殊配置项，在调用 vm.\$layer.open(option);时可以指定覆盖
****
##  联系，问题反馈
QQ群：450342630
