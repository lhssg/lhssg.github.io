# Go入门


{{< music url="../nocry.mp3" autoplay=true loop=all name=说好不哭 artist="周杰伦" >}}
 
# Go 入门

## 1.1 Hello World

helloworld.go

```go
package main

import  "fmt"

func main(){

​		fmt.Println("Hello World");

}
```

​	Go是一门编译型语言，Go语言的工具链将源代码及其依赖转换成计算机的机器指令，Go语言提供的工具都可以通过一个单独的命令go来调用。例如：

```go
go run helloworld.go //针对一次性实验 helloworld.go为文件名
```

​	此时控制台会输出Hello World。

​	如果你不只执行一次此程序，你也可以将其编译后以备不时之需，命令如下：

```go
go build helloworld.go
```

​	之后会生成一个名为helloworld的可执行二进制文件，你可以通过如下方式运行它：

```bash
./helloworld
```

​	控制台会输出Hello World

​	接下来我们来谈一下helloworld.go程序本身:

​	Go语言的代码通过package来组织，你可以将其理解为其他语言中的libraries或者modules。一个package下由同一目录下一个或多个.go文件共同构成。每个.go文件都以package声明开始，紧接着使用import关键字对一系列需要的包进行导入。之后执行存在在.go文件中的代码逻辑。

​	Go的标准库提供了100多个包，例如输入、输出、排序以及文本处理。比如helloworld.go中的fmt包，含有格式化输出、接收输入的函数。Println是fmt包中的一个基础函数，可以打印以空格间隔的一个或多个值，并在最后添加一个换行符，从而输出一整行。值得注意的是Go语言要求必须**导入恰当的包**，缺少了必要的包或导入了不需要的包，程序都无法编译通过。

​	main包是整个程序执行时的入口。通过调用其他函数来达成代码逻辑。

​	


