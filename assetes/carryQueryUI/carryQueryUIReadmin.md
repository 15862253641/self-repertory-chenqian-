# carryQuery 全局样式说明文档
## 布局
.cq-container  设置为容器：水平方向居中，宽度不为100% 左右内边距为15px 高度没有
.cq-container-fluid 宽度为100%的容器，没有外边距； 内边距为15px 上下为 0px 没有高度

# 按钮 -cq-btn
#### 普通按钮样式
 成功 cq-btn-success
 警告 cq-btn-warning
 错误 cq-btn-error
 取消 cq-btn-cancel
 确认 cq-btn-sure
 默认 cq-btn-default
 危险 cq-btn-danger
 首选 cq-btn-primary
 一般信息 cq-btn-info
 禁止按钮 cq-btn-disable
 百搭按钮 cq-btn-normal
 暖色按钮 cq-btn-warm

 #### 渐变的按钮样式
 成功 cq-btn-success-rgb
 警告 cq-btn-warning-rgb
 错误 cq-btn-error-rgb
 取消 cq-btn-cancel-rgb
 确认 cq-btn-sure-rgb
 默认 cq-btn-default-rgb
 危险 cq-btn-danger-rgb
 首选 cq-btn-primary-rgb
 一般信息 cq-btn-info-rgb
 禁止按钮 cq-btn-disable-rgb
 百搭按钮 cq-btn-normal-rgb
 暖色按钮 cq-btn-warm-rgb


#### 伪类按钮样式


- 按钮型号
大 cq-btn-bg
小 cq-btn-sm
中 cq-btn-md

- 圆角按钮 cq-btn-raduis


# 表单

## 滑块

# select 选择框

## 表格 .table
.table 表示基础表格；必须在table标签中使用；表示只有列边框的表格
.table-column 表示半边框样式
.table-striped 表示条状表格；表体的偶数行；有一定的背景颜色
.table-hover 悬浮表格
.table-condensed 紧缩表格
.table-border  边框表格
.table-inverse-striped  背景色为黑色的表格 黑色条形表格
.table-inverse-hover 黑色悬浮样式  需要依赖.table-inverse 或者 .table-inverse-striped
.table-control 表示【控制列】 固定：其他列可以滚动  .table-control 必须给table 标签 的祖籍元素添加；而不是给父元素添加

~~~css
.table-control{
  position:absolute;
}
.table-control>.table>tbody>tr>td:last-child{
  position:absolute;
  right:0;
  min-width:120px;
  text-align:center;
}
/* 选中倒数第二列，解决内容遮罩的问题 */
.table-control>.table>tr>td:nth-last-child(2)::before{
   content:"";  /*空字符*/
    width:120px;
}
.table-control>.table-box{
  overflow:auto;
}
~~~

.table-responsive  移动端表格：可以有横向滚动的效果  
.table-responsive  需要给table 的父容器添加

状态表格：给tr 添加类名
.success 成功
.info   通过
.warning  警告
.danger  危险
.primary 首选
.warm  暖色

## 栅格系统




## 分页 .Page
.pagination 实现分页样式  有 ul li a 完成的分页效果
.pagination-bgc 表示带有背景颜色的分页
.pagination-noBgc 表示没有背景颜色的分页
.pagination-inverse 黑色的分页


## 表单类
## 单选多选框样式
.circle-check  圆形选择框   .circle-check需要给input[type="checkbox"]的父元素添加
.square-check  方形选择框   .square-check需要给input[type="checkbox"]的父元素添加

~~~html
<!-- 示例代码 -->
~~~


### 滑块  .sliderbar
.sliderbar-wrap 表示进度条外围容器
.sliderbar 表示 滑块的条
.sliderbar-control 表示控制键

~~~html
  <div class="sliderbar-wrap">
    <div class="sliderbar">
        <div class="sliderbar-control">
          <span class="progress-num" id="progress-num">55</span>
        </div>
    </div>
  </div>
~~~
状态
.sliderbar-success
.sliderbar-info
.sliderbar-primary
.sliderbar-error

## 开关 .switch
.switch  开关样式的选择框   需要给  input[type="checkbox"].switch 才能实现效果

- 绿色为开  input = checked  灰色为关 input = disabled
状态
.switch-info  蓝色开 灰关
.switch-danger  红开 灰关
.switch-warning 橙色开 灰色关
.switch-primary  蓝开 红关


## 导航  .nav
注意：导航仅仅适用于 PC 端应用；且只适用于静态的样式;  导航中所有的样式都是操作li下的 a 标签设置
.nav-tab 表示像tab样式的导航条
.nav-pills 胶囊式的导航  
.nav-stacked  侧边导航

.nav-inverse  表示背景色为黑色的导航
.nav-aside   表示侧边栏导航
.nav-fixed-top  表示固定导航 在顶部
.nav-fixed-left  表示 屏幕左边固定导航
.nav-fixed-right  表示 屏幕右边固定导航


## 导航条 .navbar
注意：兼容移动端
.navbar 导航条 兼容移动端 默认样式 【隐藏】

兼容移动端样式设置规则：媒体查询最小宽度；写pc端样式；当小于这个宽度时候；使用浏览器默认样式
网站的导航条；到移动端时候可以折叠 

.navbar  导航条 兼容pc 移动
.navbar-default 给导航条添加样式  背景色
.navbar-header 有媒体查询样式；做PC 端和移动端区分； 移动端宽度100%
.collapse  元素隐藏[移动端]
.nav-collapse.collapse 在pc 端【强制】显示
.navbar-nav 表示导航条下导航
.navbar-form 表示导航条中输入框
.navbar-left 让导航在导航条中左浮动【移动端无浮动】
.navbar-right 让导航有又浮动【移动端无浮动效果】
.navbar-toggle 表示显示隐藏列表导航栏，有【右浮动】效果

.navbar-fixed-top 固定顶部导航条
.navbar-inverse 黑色导航条 border-bottom:1px solid black
   .navbar .active  背景颜色黑色  字体白色

 .breadcrumb 表示路径导航；没有基础类  
  - 每个a 添加伪元素； content:"Z/\00a0"


  ##  表单样式组件  .form-group
  1.只有表单样式  分为基础样式与可选择样式。如有特殊需要，请自定义。
  2.表单没有进行验证处理，有对验证效果的样式处理：static 状态。
  3.表单的验证需要js  正则完成。  注意：正则必须写基础正则，不要写新的正则， 因为IE 和 火狐部分版本不兼容。

  ### 表单组件基础样式
  .form-group 表示表单组件
  .form-control 控件
  .form-label 表示input 的提信息只能应用在 label 标签中

  ### 可选项表单
  .form-inline 表示横向的表单
  .form-horizontal  纵向表单
  

  ### 表单中控件
  .form-check  选择项组件  在 ul 中使用
  .form-check-item  表示多选项 在 li 中是使用
  .check-content  表示 选择的文本描述


  ### 栅格系统 .col
  栅格系统是 横向布局的处理
  提示信息：如果 父容器：不使用.row  那么自己清除浮动：计算父容器高度

  ### 屏幕
  将 .row 容器等分为12份
  .col-xs-xx   768px 以下的屏幕
  .col-sm-xx   992px 以下的屏幕
  .col-md-xx   1200px 以下的屏幕
  .col-lg-xx   1200px  以上的屏幕

  ## 分的阶段  小数点后 7位数
  1-  8.33333333%
  2-  16.6666667%
  3-  25%
  4-  33.3333333%
  5-  41.6666667%
  6-  50%
  7-  58.3333333%
  8-  66.6666667%
  9-  75%
  10- 83.3333333%
  11- 91.6666667%
  12-  100%

  ## 列偏移
  列偏移代表的属性：通过改变position：relative left值 实现列偏移
  * 代表1-12
  .col-xs-offset-*
  .col-sm-offset-*
  .col-md-offset-*
  .col-lg-offset-*

  ### 偏移量
  1
  2
  3
  4
  5
  6
  7
  8
  9
  10
  11
  12

  ### 排列
  .col-xs-pull-*  相对元素位置右边排列（往左走）
  .col-sm-pull-*
  .col-md-pull-*
  .col-lg-pull-*

  .col-xs-push-*  相对元素位置左边排列（往右走）
  .col-sm-push-*
  .col-md-push-*
  .col-lg-push-*


## 规范：
1：清空所有HTml标签的默认样式
2：字体：标准 14 px 最大 36 Px 最小 12px

3:布局 栅格系统：给一个父容器 等分多少分？

12列
  -每个子元素可以占12列中 1到12份 最大为12份 
  col-12 占据12份


  ### 开发浏览器注意事项
  1：如果您是 IE7 8 请您更换浏览器
  2：IE7 尽量全部使用 div 例如：
    - ul div.ul
    - li div.li  
    - span div.span 设置 display：inline
  3：IE7 8 不支持 浮动 清除浮动  css3 90%属性
