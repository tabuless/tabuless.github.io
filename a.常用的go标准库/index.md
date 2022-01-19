# a.常用的go标准库


## math包

### `math.IsNaN`

函数math.IsNaN用于测试一个数是否是非数NaN，math.NaN则返回非数对应的值。虽然可以math.NaN来表示一个非法的结果，但是测试一个结果是否是非数NaN则是充满风险的，因为NaN和任何数都是不相等的（在浮点数中，NaN、正无穷大和负无穷大都不是唯一的，每个都有非常多种的bit模式表示）:

```go
nan := math.NaN()
fmt.Println(nan == nan, nan &lt; nan, nan &gt; nan)
```

结果是：

```bash
false false false
```

### `math.MaxType`与`math.minType`

`math.MaxFloat32`表示float32能表示的最大数值

`math.MinFloat32`表示float32能表示的最小数值

`math.MaxFloat64`表示float64能表示的最大数值

`math.MinFloat64`表示float64能表示的最小数值

以此类推

### math/cmplx

包含了常见的复数处理函数，比如`cmplx.Sqrt(-1)`可以得到`1i`

## unicode包

提供了诸多处理rune字符相关功能的函数（比如区分字母和数组，或者是字母的大写和小写转换等），unicode/utf8包则提供了用于rune字符序列的UTF8编码和解码的功能

### unicode/utf8

1. **RuneCount(p []byte) int**

   返回p中的码点数

2. **RuneCountInString(s string) (n int)**

   统计字符串s中包含的码点数

3. **DecodeRune(p []byte) (r rune, size int)**

   解析第一个p中的UTF8的编码字符，返回该字符的编码值与字节数。如果p是空的则返回`(RuneError,0)`，否则如果编码不正确，返回返回`(RuneError,1)`

   ```go
   package main
   
   import (
   	&#34;fmt&#34;
   	&#34;unicode/utf8&#34;
   )
   
   func main() {
   	b := []byte(&#34;Hello, 世界&#34;)
   
   	for len(b) &gt; 0 {
   		r, size := utf8.DecodeRune(b)
   		fmt.Printf(&#34;%c %v\n&#34;, r, size)
   
   		b = b[size:]
   	}
   }
   ```

   输出：

   ```bash
   H 1
   e 1
   l 1
   l 1
   o 1
   , 1
     1
   世 3
   界 3
   ```

4. **func DecodeRuneInString(s string) (r rune, size int)**

   与DecodeRune类似，但是输入时一个字符串，每次调用DecodeRuneInString都会返回一个rune还有rune的UTF-8编码的字节数size 

## bytes、strings、strconv和unicode包

这四个包都是和字符串处理有关的包

## fmt

## encode


