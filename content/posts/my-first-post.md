---
title: "プログラミング始めました"
date: 2021-03-30T10:51:59+09:00
draft: false
---

# プログラミングの勉強用のブログを開設しました
このサイトは、勉強したプログラムを大雑把にまとめていきます。
プログラミング言語の多言語使いを目指して、興味あるものをつまみ食いしていきます。
手始めにGolangから手を付けます
## Golang 始めました。

{{< figure src="https://golang.org/doc/gopher/gophercolor.png" class="center" width="196" height="196" >}}
[引用：　golang.org](https://golang.org/doc/gopher/ "golang.org")

### 型と変数
まずは型と変数の宣言から始めます。
* 基本の型を見てみます。
```go
var Typ = []*Basic{
    Invalid: {Invalid, 0, "invalid type"},

    Bool:          {Bool, IsBoolean, "bool"},
    Int:           {Int, IsInteger, "int"},
    Int8:          {Int8, IsInteger, "int8"},
    Int16:         {Int16, IsInteger, "int16"},
    Int32:         {Int32, IsInteger, "int32"},
    Int64:         {Int64, IsInteger, "int64"},
    Uint:          {Uint, IsInteger | IsUnsigned, "uint"},
    Uint8:         {Uint8, IsInteger | IsUnsigned, "uint8"},
    Uint16:        {Uint16, IsInteger | IsUnsigned, "uint16"},
    Uint32:        {Uint32, IsInteger | IsUnsigned, "uint32"},
    Uint64:        {Uint64, IsInteger | IsUnsigned, "uint64"},
    Uintptr:       {Uintptr, IsInteger | IsUnsigned, "uintptr"},
    Float32:       {Float32, IsFloat, "float32"},
    Float64:       {Float64, IsFloat, "float64"},
    Complex64:     {Complex64, IsComplex, "complex64"},
    Complex128:    {Complex128, IsComplex, "complex128"},
    String:        {String, IsString, "string"},
    UnsafePointer: {UnsafePointer, 0, "Pointer"},

    UntypedBool:    {UntypedBool, IsBoolean | IsUntyped, "untyped bool"},
    UntypedInt:     {UntypedInt, IsInteger | IsUntyped, "untyped int"},
    UntypedRune:    {UntypedRune, IsInteger | IsUntyped, "untyped rune"},
    UntypedFloat:   {UntypedFloat, IsFloat | IsUntyped, "untyped float"},
    UntypedComplex: {UntypedComplex, IsComplex | IsUntyped, "untyped complex"},
    UntypedString:  {UntypedString, IsString | IsUntyped, "untyped string"},
    UntypedNil:     {UntypedNil, IsUntyped, "untyped nil"},
}
```
多い様に見えますが。bool：２値、int：整数、float：小数、complex：複素数、string：文字列　を知っていれば、最初はなんとかなりそうです。
次に変数の宣言を見てみます。

```go
var s1, s2 string // 文字型を指定

var x, y, z = 0, 1.2345, true // 変数宣言 

x := 0; y := 1.2345; z := true; // 省略記法 
```
Goは初期値により型を推定してくれます。（var を書いて＝で値を設定すればGoが勝手に文字型、整数型など型を自動的に判断してくれます。）
ただし違う型に代入する場合は変換のために型を指定します。
例えば変数xが整数の時、小数を整数に直して、代入するには次のように書きます。
var x int
x0 := 1.23

x = int(x0)
```


