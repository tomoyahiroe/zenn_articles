---
title: "macbookの環境を汚さずMAMPを入れる"
emoji: "🫧"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["MAMP", "macOS"]
published: false
---

# はじめに

諸事情により MAMP を自分の Macbook Air にインストールすることになったのですが、PC 内のグローバルの環境を汚したくありません。
環境を汚さないための方法を調べながらこの記事を書いています。

# 疑問 1：MAMP とはなんぞや

MAMP は macOS に Apache/Mysql/PHP などをまとめてインストールしてくれるもののようです。
[公式サイト](https://www.mamp.info/en/mamp/mac/)によると、

> You can install Apache, Nginx, PHP and MySQL without starting a script or having to change any configuration files! Furthermore, if MAMP is no longer needed, just delete the MAMP folder and everything returns to its original state (i.e. MAMP does not modify any of the "normal" system).

Google 翻訳にかけると、

> スクリプトを起動したり、構成ファイルを変更したりすることなく、Apache、Nginx、PHP、および MySQL をインストールできます。 さらに、MAMP が不要になった場合は、MAMP フォルダーを削除するだけで、すべてが元の状態に戻ります (つまり、MAMP は「通常の」システムを変更しません)。

だそうです。どうやら PHP や Apache, Mysql のインストールは MAMP フォルダ内にとどまるようなので安心して使えるのではないでしょうか。

最初、MAMP の存在を聞いたときはかなり怖かったので、virtualbox で別途 OS を立てて...だとか、vagrant を使って...だとかいったことを調べていたのですが、公式サイトを見逃していました。
