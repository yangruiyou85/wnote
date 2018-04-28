# go note


## 1. go程序结构
- 二进制package使用main来表示
- 库package名字跟go文件所在的目录名一样

## 2. 引入package
- 通过关键字import来引入package
- 引入pakcage,在程序中没有使用会报错，goland编辑器自动引入和删除package
- 多个包引入用()引用在一起**
> 
import (
	"os"
	"fmt"
)

## 3. go代码风格
-  go fmt -m 'xxx.go'


## 4. 常见的包

- strings

- strconv
> 提供可以在字符串和其他类型的数据之间转换的函数

- regexp
> 正则表达式引擎

- flag
> 解析命令行参数

## 5. 指针
- *T即为类型T的指针
- &t即为取变量t的地址
- *p即为取指针变量所指向的内容


## 变量的生命周期

- 垃圾回收
- 栈和堆

