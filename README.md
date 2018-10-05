# EventEmitter
<!-- EventEmitter类似于JS中的定义方法和触发方法 -->
var EventEmitter = require('events').EventEmitter; 
var event = new EventEmitter(); 
event.on('some_event', function() { //定义som_event事件
    console.log('some_event 事件触发'); 
}); 
setTimeout(function() { 
    event.emit('some_event'); //触发som_event事件
}, 1000); 

# Buffer
数据类型和数组的处理

# Stream
Stream 文件流的读写处理，可以用来做导出文件功能

# 模块系统
尽管原生模块与文件模块的优先级不同，但是都会优先从文件模块的缓存中加载已经存在的模块。

# 函数
一个函数可以作为另一个函数的参数，如下：

function say(word) {
  console.log(word);
}
function execute(someFunction, value) {
  someFunction(value);
}
execute(say, "Hello");
以上代码中，我们把 say 函数作为execute函数的第一个变量进行了传递。这里传递的不是 say 的返回值，而是 say 本身！

# 匿名函数
我们可以直接在另一个函数的括号中定义和传递这个函数：

function execute(someFunction, value) {
  someFunction(value);
}
execute(function(word){ console.log(word) }, "Hello");

我们在 execute 接受第一个参数的地方直接定义了我们准备传递给 execute 的函数。
用这种方式，我们甚至不用给这个函数起名字，这也是为什么它被叫做匿名函数 。
