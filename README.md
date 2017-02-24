# interview-treasury
面试宝典里的经典题目

## 闭包

1. **考题一：以下各程序输出几何!**
    
    
        for (var i=1; i<=5; i++) {
            (function (i) {setTimeout( function timer() {
                console.log(i);
            }, i*1000 )})(i);
        }

2.**考题二：this的指向问题!**
    
  **调用者的函数，如果该函数被某一个对象所调用，那么该函数在调用时候内部的this指向该对象。当函数独立调用的时候，那么内部的this指向undefined(非严格模式下指向window)**
    
    
    `function foo() {
         console.log(this.a)
     }
     
     function active(fn) {
         fn(); // 真实调用者，为独立调用
     }
     
     var a = 20;
     var obj = {
         a: 10,
         getA: foo
     };
     
     active(obj.getA);//输出几何`