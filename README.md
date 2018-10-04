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
<!-- Buffer 数据类型和数组的处理 -->

# Stream
<!-- Stream 文件流的读写处理，可以用来做导出文件功能 -->
