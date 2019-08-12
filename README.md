## NumScroll
#### 数字滚动累加动画插件 
1.使用前先引入jquery  (Introduce jQuery before use)  
2.加入学习Q群:814798690 (Join Learning QQ Group: 814798690)  
#### 快速使用
1.引入jquery和jquery.numscroll.js
```js
<script src="js/jquery-1.10.2.min.js" type="text/javascript" charset="utf-8"></script>
<script src="js/jquery.numscroll.js" type="text/javascript" charset="utf-8"></script>
```
2.拷贝以下布局结构 (Copy the following layout structure)
```html
<p><span id="num0"></span></p>
<p><span id="num1"></span></p>
```
3.创建numscroll对象 (Create numscroll objects)
```js
$(function() {
	//num0
	var num0 = 893623.89,addNum0,newNum0;
	$('#num0').text(num0);
	setInterval(function() {
		addNum0 = Math.random()*1000;
		newNum0 = (parseFloat(num0) + parseFloat(addNum0)).toFixed(2);
		num0 = newNum0;
		$('#num0').numScroll({
			number: newNum0
		})
	}, 1500)
	
	//num1
	var num1 = '893692813.89',addNum1,newNum1;
	$('#num1').text(num1);
	setInterval(function() {
		addNum1 = Math.random()*10000;
		newNum1 = (parseFloat(num1) + parseFloat(addNum1)).toFixed(2);
		num1 = newNum1;
		$('#num1').numScroll({
			number: newNum1,
			symbol: true
		})
	}, 1800)
})
```
#### API文档
可选参数 Parameter |  默认值 Default | 说明 Introduce
--        |    --   | --
number    |   0  | 显示值
step      |   1  | 步长
time      |   2000  | 限制用时(为null时不限制) Limited use time
delay     |   0     | 延迟开始 delay
symbol    |   false | 是否显示分隔符 display separators
#### 案例展示
![查看演示](https://github.com/chaorenzeng/jquery.numscroll.js/blob/master/index.gif)
