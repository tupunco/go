
## 命令

```
# 编译 go
make.bat -v --no-clean

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
 func Smallest<type T comparable>(s []T) T {
 	r := s[0] // panic if slice is empty
 	for _, v := range s[1:] {
 		if v < r { // INVALID, cannot compare v < r (operator < not defined for T)
 			r = v
 		}
 	}
 	return r
 }

```

