# JSON

21世纪初，`Douglas Crockford`寻找一种简便的数据交换格式，能够在服务器之间交换数据。当时通用的数据交换语言是XML，但是Douglas Crockford觉得`XML`的生成和解析都太麻烦，所以他提出了一种简化格式，也就是`JSON`

---

JSON的规则：

```
+ 并列的数据之间用逗号 `,` 分隔
+ 映射用冒号  `:` 表示
+ 并列数据的集合（数组`array`）用方括号 `[]` 表示
+ 映射的集合（对象`object`）用大括号 `{}` 表示 
```

### javascript

在`javascript`中，关联数组就是对象，对象就是关联数组。这点与`PHP`语言完全不同，在`PHP`中，关联数组也是数组。

---

数组表示 **有序** 数据的集合，对象表示 **无序** 对象的集合。如果数据的顺序很重要，那就用数组，否则就用对象。

---

### php

开发互联网应用程序，特别是编写`API`,学习`PHP`对`JSON`支持是必须要了解的知识。[see more](http://php.net/manual/en/book.json.php "php中的json")

PHP原生提供`json_encode()`,`json_decode()`函数用于编码与解码。

+ json_encode()

	该函数主要用来将数组和对象，转换为json格式。
下面是数组转换的例子：
```php
$arr = array ('a'=>1,'b'=>2,'c'=>3,'d'=>4,'e'=>5);
echo json_encode($arr);
```

结果为

```php
{"a":1,"b":2,"c":3,"d":4,"e":5}
```

下面是对象转换的例子：

```php
$obj->body = 'another post';

$obj->id = 21;

$obj->approved = true;

$obj->favorite_count = 1;

$obj->status = NULL;

echo json_encode($obj);
```

结果是：
```php
{
	"body":"another post",
	
	"id":21,
	
	"approved":true,
	
	"favorite_count":1,
	
	"status":null
} 
```

**NOTE**

由于json只接受`utf-8`编码的字符，所以`json_encode()`的参数必须是utf-8编码，否则会得到空字符或者null。当中文使用`GB2312`编码，或者外文使用`ISO-8859-1`编码的时候，这一点要特别注意。

PHP支持两种数组，一种是只保存"值"（value）的索引数组（indexed array），另一种是保存"名值对"（name/value）的关联数组（associative array）。

由于`javascript`不支持关联数组，所以`json_encode()`只将索引数组（`indexed array`）转为数组格式，而将关联数组（`associative array`）转为对象格式。

比如，现在有一个索引数组

```php
$arr = Array('one', 'two', 'three');

echo json_encode($arr);

//result:
["one","two","three"]
```

如果将它改为关联数组：

```php
$arr = Array('1'=>'one', '2'=>'two', '3'=>'three');

echo json_encode($arr);

//result:
{"1":"one","2":"two","3":"three"}

//注意，数据格式从"[]"（数组）变成了"{}"（对象）
```

[see more](http://www.ruanyifeng.com/blog/2011/01/json_in_php.html "阮一峰博客")