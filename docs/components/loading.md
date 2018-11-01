# Loading 加载组件
----
### 基础用法
使用```width```、```height```、```color```、```fullScreen```、```border-width```、```vertical```和```has-text```属性来定义 Loading 的样式。
``` html
<kk-loading></kk-loading>
<!-- 自定义定位右上角 -->
<kk-loading class="right-top-loading" width="20" height="20" color="#ed3f14"></kk-loading>
<kk-loading has-text>自定义文字</kk-loading>
<!-- 测试开启 -->
<kk-loading has-text fullScreen>全屏的loading</kk-loading>
<kk-loading has-text vertical>垂直的loading</kk-loading>
```

### 属性
| 参数      | 说明    | 类型      | 可选值       | 默认值   |
|---------- |-------- |---------- |-------------  |-------- |
| width     | 设置大小   | String  |    — | -   |
| height    | 设置大小   | String  |    — | -   |
| color     | 颜色   | string    |  自定义 |     —    |
| has-text     | 是否有文字   | Boolean  |    — | false   |
| fullScreen     | 是否为全局效果   | Boolean  |    — | false   |
| vertical     | 垂直排列icon和文字   | Boolean  |    — | false   |
