# Game Math

## Number representation

$Rep(A)$表示最接近A的表示
理想情况下,$Rep(A) = A$, $Rep(x)$ 是多对一的映射
$$
AbsError\ = \ |Rep(A)-A| \\
RelError\ = \ \bigg|\frac{Rep(A)-A}{A}\bigg|
$$

- 32bit single precision floating point
  - 1sign 8exponent 23fraction
  - fraction represent 1.xxxx, the $xxxx$ part
  - $2^8-1=\text{0xFF},[0,255]$ $\lfloor\frac{255}{2}\rfloor=127$, the bias is 127 $[-127,128]$, reserved maxinum and mininum, then $[-126,127]$


$RelError_a \req \frac{1}{2^24} $
浮点数的相对误差是确定的,

### Arithmetic Operation
