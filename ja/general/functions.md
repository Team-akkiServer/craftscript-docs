---
title: Functions/関数
layout: default
parent: General
---

基本的な関数宣言は、以下のようになります。
```craftscript
func main(): int { ... return 0; }
```
void(何も返さない)場合は、`func main(): void`のような宣言にするか、`: void`の部分を省略するとデフォルトでvoid型を返すようになります。

アクセス修飾子もつけられます。
```craftscript
priv func privateFunction() { ... }
```
さらに、nullable/nonnull/notnullが利用可能です。
```craftscript
nonnull func nullableFunction(nullable text: string, notnull i: int) { ... }
```
nonnullはnullを返すとエラーになります。
```craftscript
nonnull func errorFunc() {
    return null; //エラー
}