[![N|Solid](img/safs_logo.png)](https://www.cn-abs.com/Market/MarketSummary.aspx)

# 关于IE8浏览器下的兼容性测试

#### 2017/4/10

`DengDeng`&`HaoYu`&`WenTing`

## IE8下的兼容性bug清单：

| 控件/页面 | 备注 | 原因 | 状态 |
| ------- | ----- | ----- | ---- |
| 通用页面模版中`面包屑导航`模块| jquery库中`trim()`方法IE8以下不支持 | 项目中调用该方法 | 已修复 |
| 所有应用`<select>`标签的页面变白 | IE9以下不支持`<select>`标签的样式设置 | css hack 兼容处理 | 已修复 |
| 所有应用`<select>`标签的高度失灵 | IE中`<select>`标签的样式必须设置height，chrome下默认为line-height | 定义height:24px | 已修复 |
| 统计数据 | IE8下信息图表插件`highstock.js`无法渲染 | charttheme.js中未配置图例的fontWeight，默认为null报错| 已修复 |
| 信息配置>投资收益 | 数据列表横向滚动条消失 | IE下overflow:auto缺省引起 | 已修复 |
| 所有应用select2.js的页面 | IE8页面复选框全部`失效` | 页面中ret.`delete`作为关键字不支持IE8 | 已修复 |
| 投资组合 | `getElementsByClassName()`方法不支持低版本IE | Object doesn't support property 'getElementsByClassName'| 未修复 |


## 如何解决前端渲染中，兼容IE8的问题。