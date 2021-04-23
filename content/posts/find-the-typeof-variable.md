---
title: "変数のタイプを調べる"
date: 2021-04-23T13:03:09+09:00
draft: false
---
## 変数のタイプを調べる方法3種類
- Printfで%Tを使う
- reflect.TypeOf()関数を使う
- reflect.ValueOf().Kind()関数を使う

```go
package main

import (
	"fmt"
	"reflect"
)

func getType1(i interface{}) {
	fmt.Printf("Type is %T\n", i)
}

func getType2(i interface{}) {
	fmt.Printf("Type is %v\n", reflect.TypeOf(i))
}

func getType3(i interface{}) {
	fmt.Printf("Type is %v\n", reflect.ValueOf(i).Kind())
}

func main() {
	fmt.Println("//$T version")
	getType1(10)
	getType1(0.1111)
	getType1(true)
	getType1("Hello")
	fmt.Println("----------------------")

	fmt.Println("//reflect.TypeOf version")
	getType2(10)
	getType2(0.1111)
	getType2(true)
	getType2("Hello")
	fmt.Println("----------------------")

	fmt.Println("//reflect.ValueOf.Kind version")
	getType3(10)
	getType3(0.1111)
	getType3(true)
	getType3("Hello")
}
```
実行結果
```go
//$T version
Type is int
Type is float64
Type is bool
Type is string
----------------------
//reflect.TypeOf version
Type is int
Type is float64
Type is bool
Type is string
----------------------
//reflect.ValueOf.Kind version
Type is int
Type is float64
Type is bool
Type is string

```
