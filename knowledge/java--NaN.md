# java的NaN


### 在java浮点数值计算都遵循IEEE 754规范，具体来说，下面是用于表示溢出和出错情况的三个特殊的浮点数值：

+ 正无穷大(Double.POSITIVE_INFINITY)
+ 负无穷大(Double_NEGATIVE_INFINITY)
+ 不是一个数字(Double.NaN,Not-a-Number)

### NaN的产生
+ 0.0/0 (整数/0 不会产生NaN,程序会报ArithmeticException: / by zero异常)
+ Double.parseDouble("NaN")
+ 负数的平方根: Math.sqrt(-1)
例如，一个正整数除以0的结果为正无穷大，计算0.0/0或者负数的平方根结果为NaN。


### 检测一个特定值是否等于Double.NaN
Double.isNaN(d)
d==Double.NaN false