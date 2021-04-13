---
title: "無限ループ"
date: 2021-04-13T15:02:59+09:00
draft: false
---

## for文による無限ループ（終わらない繰り返し）

無限の繰り返し、ファイルinfinite-loop.goとして、エディタで次のコードを書きます。
```go
package main

import "fmt"

func main() {
        for {
          fmt.Println("無限ループ： Ctrl+C1で停止")
        }
}
```
実行結果は
```bash
$ go run infinite-loop.go
無限ループ： Ctrl+C1で停止
無限ループ： Ctrl+C1で停止
無限ループ： Ctrl+C1で停止
無限ループ： Ctrl+C1で停止
無限ループ： Ctrl+C1で停止
..........
無限ループ： Ctrl+C1で停止
無限ループ： Ctrl+C1で停止
