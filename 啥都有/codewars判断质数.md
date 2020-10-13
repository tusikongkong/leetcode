首先定义一下质数：

* 负数全不是质数
* 0和1不是质数，2是质数

那么现在要做的就是对于

`for(let i=3;i < ?;i+=2)`

循环要做到减少时间复杂度

一开始取？为：

`num/2`

但始终报 `Time out`

百度得应该是开平方，即：

`Math.sqrt(num)`

通过

```
function isPrime(num) {
  if(num==2||num==3||num==5||num==7) return true;
  if(num==0||num==1||num<0||num%2==0||num%3==0||num%5==0||num%7==0) return false;
  
  for(let i=3;i<=Math.sqrt(num);i+=2){
    if(num%i == 0) return false;
  };
  return true;
}
```

