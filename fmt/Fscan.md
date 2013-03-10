# func Fscan(r io.Reader, a ...interface{}) (n int, err error)

参数列表

- r 输入文件指针
- a... 值变量列表

返回值：

- 返回成功读取的参数的数量 n
- 返回error

功能说明：

>这个函数主要是从指定文件读取文本，将空白分割的连续数据顺序存入参数里。
>
>换行视同空白。它返回成功读取的参数的数量。
>
>如果少于提供的参数的数量，返回值err将报告原因。
>

代码实例：

        package main

        import  "fmt"
        import  "io"

        func main(){
                str := "34  343  245"
                var a,b,c int
                fmt.Fscan(io.Stdin,&a,&b,&c)
                fmt.Println(a,b,c)
        }

