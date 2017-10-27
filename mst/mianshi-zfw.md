 # h2 面试
 ## 内容
 ### 1.  js数据类型
    * 简单类型: String, Number, Boolean, Undefined
    * 引用类型: Function Object

 ### 2. 简单类型和引用类型比较
    * 简单类型数据存放在栈内存中, 引用类型数据存在堆内存中


 ### 3. 函数对象跟原生对象有哪些不一样地方,或者说少了什么东西?


 ### 4. 函数对象有什么属性和方法?


 ### 5. 怎么判断一个引用是不是一个数组?
    *  用Array.isArray() 判断, 返回真为数组.
    *  var b = {"name": "2"};
       console.log((b.constructor == Array)); // 输出为true

 ### 6. instanceof 判断原理

    *  instanceof表示的就是一种继承关系.
    *  Instanceof运算符的第一个变量是一个对象，暂时称为A；第二个变量一般是一个函数，暂时称为B
    * 沿着A的__proto__这条线来找，同时沿着B的prototype这条线来找，如果两条线能找到同一个引用，即同一个对象，那么就返回true。如果找到终点还未重合，则返回false。

 ### 7. ES6 相对于 ES5 多出了什么内容?


 ### 8. 箭头函数特点(为什么用箭头函数?少写funtion外多出了什么特性?)

 ### 9. 不用api,自己实现浅拷贝
    ```
    const obj1 = {
      "name":"lisi",
       "age": 22,
     "arr": [1,2,3]};

     function lowerCopy(obj) {
        const ob = {};
        for(var elem in obj ){
          if(obj.hasOwnProperty(elem)) {
            ob[elem] = obj[elem];
          }
        }
        return ob;
     };

     var obj2 = lowerCopy(obj1);
    ```
 ### 10. 浅拷贝和深拷贝实现各自思路

 ### 11. 原生实现深拷贝
  ```
  1 递归实现深拷贝

  function deepCopy (initObj, endObj) {
  const obj = endObj || {};

  for(let i in initObj) {
    var prop = initalObj[i]; // 避免相互引用对象导致死循环，如initalObj.a = initalObj的情况
    if(prop === obj) {            
      continue;
    }     

    if(typeof initObj[i] == 'object') {
      initObj[i].constructor === Array ? [] : {};
      arguments.callee(initObj[i], obj[i]); //包含当前执行函数,用于递归调用
    }
    else {
      obj[i] = initObj[i];
    }
  }
  return obj;
}

var a = {};
var obj1 = {"name": "lisi", "age": 1, "arr": [1, 2, 3]};
var obj2 = deepCopy(obj1, a);
obj2.arr = [3, 4,5];
console.log(obj1);  //对象obj2.arr改变数据,但obj1.arr=[1,2,3] ,说明深拷贝成功

  ```

 ### 12. http包熟悉情况, 头部有什么字段

 ### 13. get 和 post 自定义头部

 ### 14. 跨域, ajax交互时, http头部有什么特性字段?

 ### 15. React 生命周期有哪些?(按组件加载顺序)

 ### 16. 如果有异步,你会把它放到哪个生命周期部分让它执行?(或者说把它放    在ComponentDidMount和ComponentWillMount区别)

 ### 17. setState对api了解

 ### 18. setState实现和特性

 ### 19. 初始化一个count = 1, 在后面触发一个事件调用handleChange方法, 这个方法连续执行3次setState, 问最后输出count结果
  ```
 getInitialState: function(){
                    return {count: 1 };
                },
                handleChange: function(event){
                    this.setState({count: count +1});
                    this.setState({count: count +1});
                    this.setState({count: count +1});
                },
  ```
 ### 20. 上面结果为count = 1 的原因 , 为什么setState只渲染了一次

 ### 21. 同时使用 React 和bootstrap, 你是怎么结合的?

 ### 22. 在React 使用的ui有哪些? Sementic 是基于什么做的?

 ### 23. 移动端性能优化有哪些

 ### 24. 单从打包角度来说,过程有哪些来提升文件效率(或者说打包过程中,配置文件,有什么作用)

 ### 25. node.js怎么删除一个文件?

 ### 26. mongodb 数据库缓存有没有涉猎?(有没有什么接口缓存)

 ### 27. 写css 时, 有什么要注意的(在项目有大量css代码时这种情况)

 ### 28. 在渲染过程中, 一个标签嵌套多个标签,多了会出现什么结果(比如: 一个标签嵌套2个标签, 另一个标签嵌套3个标签)
