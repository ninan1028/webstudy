### 记录array的方法

### 1 slice()

 slice() 方法返回一个从开始到结束(不包含结束)选择的数组的一部分浅拷贝到一个新数组对象

**原始数组不会被改变**

~~~~
 let a=[1,2,3,4];
 let sliced=a.slice(1,3);
 console.log(a); // [1,2,3,4]
 console.log(sliced) // [2,3]
~~~~



#### 描述

  slice不修改原数组,只会返回一个浅复制了原数组中的元素的一个新数组.原数组的元素会按照下述规则进行拷贝:

* 如果该元素是个对象引用(不是实际的对象) 在这里实际对象表示什么 ?,slice会拷贝这个对象引用到新的数组里.两个对象引用都引用了同一个对象.如果被引用的对象发生改变,则新的和原来的数组中的这个元素也会发生改变
* 对于字符串,数字及布尔值来说(不是String Number 或者Boolean对象),slice会拷贝这些值到新的数组里,在别的数组里修改这些字符串或者数字或者布尔值,将不会影响另一个数组.





**类似数组(Array-like)对象**

slice方法可以将一个类数组(Array-like)对象集合转换为一个数组.你只需将该方法绑定到这个对象上,

~~~~
function list(){
  return Array.prototype.slice.call(arguments);
}
var list1=list(1,2,3);
~~~~

除了使用Array,prototype.slice.call(arguments),也可以简单的使用[].slice.call(arrguments) 来代替.

***



