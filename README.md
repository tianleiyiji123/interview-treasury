# interview-treasury
面试宝典里的经典题目

## 闭包

1. **考题一：以下各程序输出几何!**
    
    
        for (var i=1; i<=5; i++) {
            (function (i) {setTimeout( function timer() {
                console.log(i);
            }, i*1000 )})(i);
        }