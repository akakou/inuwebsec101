---
layout: page
title: 静的ページと動的ページ
parent: Webアプリケーションの仕組み
nav_order: 3
permalink: /webapp/active-page/
---

# 静的ページ・動的ページ

前提ページ：[クライアントサーバモデル](../client-server-model/)  
推奨ページ：[ウェブページの仕組み](../webpage/)

セキュアな Web サイトの作り方を学ぶ上で、Web サイトがどのように通信をしているかを知ることは重要です。このページでは 静的ページと動的ページの違いについて学びます。

---

## 静的ページ

クライアントから HTTP リクエストを受けたとき、サーバに格納されているファイルをそのまま返す Web ページのことを、静的な Web ページであるといいます。
（[クライアントサーバモデル](../client-server-model/) ではこのようなサイトを想定していました。）

### 静的ページのイメージ

クライアントは `hello.html` をリクエストとして送信し、サーバはそのまま `hello.html` をレスポンスとして返している。

#### 猫が静的サイトにアクセスする例

![]({{ '/assets/images/passive-neko.png' | relative_url }})

## 動的サイト

クライアントから HTTP リクエストを受けたとき、サーバが利用者や HTTP リクエストのボディの入力等※1 に合わせて、HTTP レスポンスの内容を変更する Web ページを、動的な Web ページと呼びます。

### 動的サイトのイメージ

リクエストのパラメータ ( `name=neko` か `name=usagi` )によって、レスポンスが変わっています。 ※2

#### 猫が動的サイトにアクセスする例

![]({{ '/assets/images/active-neko.png' | relative_url }})

#### うさぎが動的サイトにアクセスする例

![]({{ '/assets/images/active-usagi.png' | relative_url }})

## 備考

※1 他にもデータベースの中身や、サーバの状態、外部 API を叩いた結果等が考えられます。

※2 このようなパラメータに関する説明は、今後別のページで行います。

※ 静的ページや動的ページの定義については、多少曖昧なところがあります。  
動的と静的なページの違いだけわかっていただけたら幸いです。