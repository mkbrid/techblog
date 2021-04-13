---
title: "繰り返しWhile"
date: 2021-04-13T15:33:22+09:00
draft: false
---
## 繰り返しWhile

繰り返し、ファイルwhile.goとして、エディタで次のコードを書きます。
```go
package main

import "fmt"

func main() {
	sum := 1
	for sum < 100 {
		sum += sum
	}
	fmt.Println(sum)
}
```
実行結果は
```bash
$ go run while.go
128


