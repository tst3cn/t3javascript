# t3javascript
一个甲瓦死磕日屋外葡特裤。

## DOM操作

### 选择器
```
// 类选择器
t3.$(".xxx") 

// ID选择器
t3.$("#xxx")  

// 表单项选择器，只对表单、<iframe>、<img>有效
t3.$("input_name:xxx")
 
// ..........
// jQuery支持的选择器语法t3javas都支持

```


### 属性操作

* 当设置了自定义属性后，本页面将不在是一个合法的HTML文档，对此，HTML5提供了一个解决方案。在HTML5文档中，任意以“data-”为前缀的小写的属性名字都是合法的。这些“数据集属性”将不会对其元素的表现产生影响.
* dataset对象保存了所有dtaa属性的值，例如 data-t3 = "tang3" ， alert(dataset.t3)
   

添加一个自定义属性
```
t3.$("#xxx").attr("attrName", "属性值")
```

获取自定义属性值

```
t3.$("#xxx").attr("attrName")
```

移除属性
```
t3.$("#xxx").removeAttr("attrName")
```

判断属性是否存在
```
t3.$("#xxx").hasAttr("attrName")
```


## 函数库

1. 传入剩余秒数，传入分、秒的id并在其innerText进行倒计时
```
/**
 * 传入剩余秒数，传入分、秒的id并在其innerText进行倒计时
 * @param seconds 倒计时总秒数
 * @param minuteId 分钟数innerText所在元素的id名称
 * @param secondId 秒数innerText所在元素的id名称
 */
t3.fn.countDown(seconds, minuteId, secondId)

// 例如
剩余：<span id="m"></span>分<span id="s"></span>秒
t3.fn.countDown(300, "m", "s")
```

2. 字符串填充
```
	/**
	 * 字符串填充
	 * @param str 被填充的数字
	 * @param fill 填充物，用什么字符串去填充
	 * @param _len 填完之后字符串总长度
	 * @param _direction 填充防线，可选值：left / right，默认left
	 * @returns {string}
	 */
t3.fn.strPad(str, fill, _len, _direction) 
```




