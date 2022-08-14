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


$RelError_a \approx \frac{1}{2^{24}} $
浮点数的相对误差是确定的,

### Arithmetic Operation

#### Addition and Subtraction

$A=S_A*M_A*2^{E_A}$

1. swap A & B so that $E_A \geq E_B$

2. Right Shift $M_B$ $E_A-E_B$ bits.

3. add shifted $M_B$ to $M_A$

4. $E_{A+B} = E_A$

5. renormalized the mantissa if necessary

- if two numbers differ in exponents by more than number of matissa bits, then the smaller num will be 0 in addition.

note 
Hennessy and Patterson details about rounding

#### Multiplication

### Special Values

#### Zero

**denormals**

*hole at zero*
*flush to zero*

catastrophic cancelation  **avoid**

*deferred rendering*

## real world floating point

### Internal FPU Precision

### Performance Issue

correct | fast

- denormalized number
  - determine on specific FPU arch
- Software floating point emulation
- IEEE Specification Compliance
  -

