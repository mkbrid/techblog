---
title: "繰り返しFor"
date: 2021-04-13T12:25:45+09:00
draft: false
---

## for文による繰り返し

繰り返し、ファイルfor.goとして、エディタで次のコードを書きます。
```go
package main

import "fmt"

func main() {
    sum := 0 
    for i :=0; i<10; i++ {
      sum += i
    }
    fmt.Println(sum)
}
```
実行結果は
```bash
$ go run for.go
10
//1+2+3+4+5
