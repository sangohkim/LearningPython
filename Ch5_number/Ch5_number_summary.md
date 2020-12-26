# Summary1. Number type
Number in python, means a collection of similar types.  
For example, generic numbers, literals expressions, and so on.  
### Number Literals
> In this sections, I wrote some literals that express number.
1. Integers  
    1) Python provides *infinite precision* in integer type.  
        <pre><code>>>> 99999999999999999999999999999999999999999999999 + 1
       10000000000000000000000000000000000000000000000000000</code></pre>  
    2) Binary, Octal, Hex
        * Binary: Python allows two prefixes, *0b*, *0B*.
        * Octal: *0o*, *0O*
        * Hex: *0x*, *0X*
2. Floating point  
Float in Python is similar to *double* in C.

### Expressions operators
> This section contains my several recommendations which will be helpful to make programs unaffected by versions and efficient.
1. Use '!=' to compare(not '<>')
2. X < Y > Z available (X < Y and Y > Z)
3. the value of *1 == 2 < 3* is False  
Because 1 == 2 is False.
4. 2.0 > 1 == 2.0 > 1.0
You should be careful about *casting*.

### Division
> This sections contains differences in division methods which depends on versions.
1. X / Y
    <pre><code>>>>3 / 2
   1       (2.X, Classic Division)
   1.5     (3.X, True Division)
   >>> 3.0 / 2
   1.5     (2.X)
   1.5     (3.X)</code></pre>
2. X // Y
    <pre><code>>>> 3 // 2
   1       (2.X)
   1       (3.X)
   >>> 3.0 // 2
   1.0     (2.X)
   1.0     (3.X)</code></pre>  
To make your program not affected by versions, use '//' and set operands always *float*

### Imaginery Number
> Brief informations about imaginery numbers.  
<pre><code>>>> 1 + 2j
1 + 2j
>>> complex(1, 3)
(1 + 3j)</code></pre>

### Bit
> Brief informations about dealing with bits in python    

&, |, ^ available

### Fractions
> Some example codes about Fraction objects.
>> This objects are constrained by the floating point hardware performance.
<pre><code>from fractions import Fraction
x = Fraction(1, 3)
y = Fraction(1, 4)     # y = Fraction('.25') = Fraction.from_float(0.25)
z1 = x + y             # z1 = Fraction(7, 12)
z2 = x - y             # z2 = Fraction(1, 12)  
z3 = x * y             # z3 = Fraction(1, 12)
z4 = x / y             # z4 = Fraction(4, 3)
z5 = x // y            # z5 = 1
</code></pre>
<pre><code>from fractions import Fraction
z = Fraction(*f.as_integer_ratio(2.5))
</code></pre>

* *Fraction + integer -> Fraction*
* *Fraction + float -> float* 

### Decimal
> Some example codes about Decimal objects.
>> This objects are constrained by the floating point harware performance.
<pre><code>from decimal import Decimal
x1 = Decimal('0.25')
x2 = Decimal(0.25)
x3 = Decimal.from_float(0.25)
</code></pre>

### Boolean
> True: 1, False: 0

### Etc.
abs, round, floor(math module), sqrt(math module)  
random(random module)

### Questions
1. Why?(아래 프로그램에서 정밀도는 4자리까지로 고정되어 있음.)
    <pre><code> from decimal import Decimal
    Decimal(0.1) + Decimal(0.1) + Decimal(0.1) - Decimal(0.3)
    # result: Decimal('1.110E-17')
    Decimal('0.1') + Decimal('0.1') + Decimal('0.1') - Decimal('0.3')
    # result: Decimal('0.0')</code></pre>


