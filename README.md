## 如何高效的命名你的项目
### 1.文件夹命名
* 1.最好用一个单词描述

| 常用项目命名 | omi、element、master、project、test、vue、iview |
|:-------:|:---------:|
| 二级目录 | build、static、config、src、examples、base、common、issues、assert |
| 三级目录 |libs、models、plugins、skins、images、css、js |

* 2.如果一个单词描述不了，名词加动词

color-pick、button-groups、date-picker、option-grounp、jquery-select、jquery-swiper

* 3.中间用-或者_连接为了方便归类、一目了然
>node_models、async-demo、array-union、array-differ、babel-each。

### 2.文件命名
* 1.最好用一个单词描述

>以下变量名可以加css、js、html，例如index.html、index.js、index.css。

| 常用组件命名 | index、message、menu、slider（滑块）、page、progress（进度条）、tooltip（提示）、tree、upload、time、button、checkbox、dialog、cascader（三级联动） |
|:-------:|:---------:|
| 常用文件命名 | index、shopping（购物）、 share（分享）、integral（积分）、advertisement（广告）、pay（支付）、community（社区）、game、docs、bussiness|

* 2.如果一个单词描述不了，名词加动词

share-to-friends，share-to-community，weex-pay，alipay-pay，user-integral，
game-page，docs-page等等反正就是自我想象。

* 3.中间用-或者_连接为了方便归类、一目了然

>在目前做的pc端和移动端，简单的对他们分个类：
* 1.移动广告(mobile-advertisement)
* 2.移动社交(mobile-social)
* 3.移动电子商务(mobile-bussiness)
* 4.手机游戏(mobile-game)
* 5.手机电视(mobile-tv)
* 6.移动电子阅读(mobile-reading)
* 7.手机搜索(mobile-search)
* 8.移动支付(mobile-pay)
* 9.手机内容共享(mobile-share)

关于以上的项目都可以用名词+需要的动词命名，达到见词知意

### 3.html布局命名

[可以参考DIV+CSS规范命名大全集合](http://www.divcss5.com/jiqiao/j4.shtml)但是我觉得写的并不是很好，很全面。因为往往比较纠结的是每一个大布局中小布局的命名。

| 外套 wrap|  #container|
|:-------:|:---------:|
| 头部 header| #head, #header，#nav，#sub-nav，#menu， #sub-menu，#branding|
| 主要内容 main |bussiness-title 、bussiness-logo、bussiness-search、bussiness-search-results|
| 左侧 main-left |#side-bar, #side-bar-a, #side-bar-b |
| 右侧 main-right |#side-bar, #side-bar-a, #side-bar-b |
| 内容 content | radio-click、radio-heightlight、radio-active、input-seach-off、input-search-on |
| 底部 footer|#service, #regsiter,#partner（合作伙伴）,#joinus, #site-info|

>总结

* 1.一般头部有nav、nav-event、nav-style、nav-item、nav-link。
* 2.内容：xx-title、xx-box、xx-warp、xx-item、xx-item-title、xx-item-link、xx-item-image
* 3.底部：footer-time、footer-box、footer-item、footer-item-link、footer-address。总之xx-wrap，xx-box，xx-item、xx-link、xx-title、xx-total肯定会满足你80%的需求

### 4.js变量命名
* 1.基础类型和引用数据类型（基础类型 
> * 字符串var s_count="",
> * 布尔类型var b_status=false,
> * 数字类型var n_total=12。
> * 引用数据类型 
> * 数组var ar_bar=[],
> * 对象var o_bar=[],
> * 函数var f_submit=function(){}）
* 2.不要用关键字命名default、class、private

* 3.用可读的同义词代替保留词。
```
// bad
var superman = {
  class: 'alien'
};

// bad
var superman = {
  klass: 'alien'
};

// good
var superman = {
  type: 'alien'
};
```
* 4.函数用驼峰形式（动词+名词）

login(),logout(),expandList(),getTotal(),keySearch(),submitForm(),cancel(),goMore(),searchAll(),searchCurrent().clearContent().uploadImage().searchResult()这些都是常用事件，可以清晰知道每一项的意义。

[es5的语法规范](https://github.com/airbnb/javascript/tree/es5-deprecated/es5)

* 5.当命名的构造函数和类使用PascalCase。
```
// bad
function user(options) {
  this.name = options.name;
}

var bad = new user({
  name: 'nope'
});

// good
function User(options) {
  this.name = options.name;
}

var good = new User({
  name: 'yup'
});
```
* 6.不要使用尾随或前导下划线。
```javascript
// bad
this.__firstName__ = 'Panda';
this.firstName_ = 'Panda';
this._firstName = 'Panda';

// good
this.firstName = 'Panda';
```
* 6.前缀jQuery对象变量与$。
```
// bad
var sidebar = $('.sidebar');

// good
var $sidebar = $('.sidebar');

// bad
$('ul', '.sidebar').hide();

// bad
function setSidebar() {
  $('.sidebar').hide();

  // ...stuff...

  $('.sidebar').css({
    'background-color': 'pink'
  });
}

// good
function setSidebar() {
  var $sidebar = $('.sidebar');
  $sidebar.hide();

  // ...stuff...

  $sidebar.css({
    'background-color': 'pink'
  });
}

// bad
$('.sidebar').find('ul').hide();

// good
$('.sidebar ul').hide();

// good
$('.sidebar > ul').hide();

// good
$sidebar.find('ul').hide();

```
### 5.css命名
| 公共的| common.css |
|:-------:|:---------:|
| 其实和common差不多 | base.css |
| 动画 | animation.css |
| 皮肤 | skin.css |
| 文字 |  font.css  |
| 主题  |  themes.css |
| 打印样式 | print.css | 
| 颜色 | color.css |

### 6.图片命名

* 1、第一部分是图片的逻辑归属分类
* 2、第二部分是图片的表现内容
* 3、第三部分是图片的内容的类型（有些图片还会有第四部分，表示图片表现的状态。）
* 4、tabbar_home_icon, navigationbar_showtime_icon@2x.png，tabbar_categories_icon

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2604175-a2e22023e6d03304.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 7.分享demo

* 1.饿了么部分组织构架

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2604175-a3ada75909695d03.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 2.腾讯omi

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2604175-8952b3717f46fff3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
