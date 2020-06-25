
## 命令

```
# 运行
go tool go2go run monoid.go2

# 翻译
go tool go2go translate monoid.go2
```

## 参考
- https://gocn.vip/topics/10567
- https://colobu.com/2020/06/17/type-parameters-in-go-generic/
- https://colobu.com/2020/06/18/run-local-go-generic-files/
- https://tonybai.com/2020/06/18/the-go-generics-is-coming-and-supported-in-go-1-17-at-the-earliest/

## 问题

```
// ------------------
t := time.Now()
switch {
case t.Hour() < 12: //missing ',' in argument list
    fmt.Println("It's before noon")
default:
    fmt.Println("It's after noon")
}

// ------------------
func Reverse <type T> (list []T) {
	i := 0
	j := len(list)-1
	for i < j {
		list[i], list[j] = list[j], list[i] //expected '==', found '='
		i++
		j--
	}
}

```

