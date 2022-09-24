---
title: "NestJS エラー集(自分用)"
emoji: "😇"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["NestJS", "TypeScript", "classvalidator", "エラー"]
published: false
---

# はじめに

NestJS の学習中につまづいたエラーをメモするための記事です。随時増えていくと思います。
立ち位置としては自分のメモ用ですが、同じエラーにぶち当たった方の役に立てればいいなぁと心の片隅でほんの少しくらい思いながら書いてます。

# エラー集

## class-validator

### @IsEnum() エラー

バリデーション用のライブラリである class-validator の@IsEnum 　デコレータを使用した際に発生しました。

problems(問題)のエラー文

```
Unalbe to resolve segnature of property decorator when called as an exception

Expected 2 arguments, but got 1
```

架空のコードが以下になります。

```ts hoge-status.dto.ts
import { isEnum } from "class-validator";
export class HogeStatusDto {
  @isEnum(HogeStatus)
  status: HogeStatus;
}
```

**isEnum を IsEnum 　のようにアルファベットの i を 大文字にすると解決しました。**

[参考](https://www.angularfix.com/2022/05/unable-to-resolve-signature-of-property.html)
