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

### Decimal

### Etc.
abs, round, floor(math module), sqrt(math module)  
random(random module)


