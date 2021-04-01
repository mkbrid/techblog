---
title: "簡単な プログラム"
date: 2021-04-01T16:47:20+09:00
draft: true
---

## 簡単なプログラミムを書いてみます
ファイル名を01-simle-program.goとして、エディタで次のコードを書きます。
```go
package main

import "fmt"

func main() {
    fmt.Println("こんにちは")
}
```
実行結果は
```bash
$ go run 01-simple-program.go
こんにちは
```
次に、前回変数について学んだので四則演算をやってみます。
02-sisokuenzan.go
```go
package main

import "fmt"

func main() {
    x, y := 10.0, 20.0
    wa := x + y
    sa := x - y
    kake := x * y
    wari := x / y
    fmt.Printf("x + y = %f\n", wa)
    fmt.Printf("x - y = %f\n", sa)
    fmt.Printf("x * y = %f\n", kake)
    fmt.Printf("x / y = %f\n", wari)
}
```

実行結果
```bash
x+y = 30.000000
x+y = -10.000000
x+y = 200.000000
x+y = 0.500000
```


