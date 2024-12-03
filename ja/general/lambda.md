---
title: Lambda/ラムダ式
layout: default
parent: General
---

ラムダ式は、無名関数の定義なのでFunction型になります。

宣言は以下のようになります。
```craftscript
var lambda: Function = () => { ... };
lambda.run();
```
現状、オブジェクト指向の実装ができていないので値を返すことはできません。

---


今後の実装では以下のような文をサポートする予定です。

```craftscript
var lambdaV2: Function<Int> = (a) => { return 1 + Int.of(a); };
var result: int = lambdaV2.run();
io.out.println("Result: " + result);
```

引数に関しては、()内のものはすべてobjectなので変換する必要がありますが...

この実装は少し考えます。