# CETEIceanとMiradorを使用したTEI/XMLビューア

## 概要

TEI/XMLファイルを読み込み、Miradorで画像を表示し、CETEIceanでテキストを表示するサンプルアプリを作成しました。以下のURLからお試しいただけます。

**デモサイト**

<https://nakamura196.github.io/ceteicean-mirador/>

![アプリのスクリーンショット](https://storage.googleapis.com/zenn-user-upload/f60a3027c6fd-20250314.png)

## 背景

これまでにも、同様の機能を提供するアプリケーションを開発してきました。

- **Next.js を使用した実装例**  
  https://zenn.dev/nakamura196/articles/a959b7bda6d4da

- **XSLT を使用した実装例**  
  https://zenn.dev/nakamura196/articles/d0e74f0e3fc547

今回は、HTMLとプレーンなJavaScriptのみを使用して実装する方法をご紹介します。

## 対象データ

以下の校異源氏物語テキストDBを対象とします。

https://kouigenjimonogatari.github.io/

## 実装方法

ソースコードは以下のリポジトリで公開しています。

https://github.com/nakamura196/ceteicean-mirador

### 実装のポイント

#### 1. CETEIcean の `behaviors` を利用した `pb` タグの処理

CETEIcean の `behaviors` を利用して `pb` タグのクリック時の挙動を定義しています。

#### 2. Mirador でのページ遷移処理

`pb` タグをクリックした際に、TEI/XML ファイルから `Canvas` の URI を取得し、Mirador のページ遷移を実行します。

#### 3. CETEIcean の CSS を利用

テキストのスタイルは、CETEIcean が提供する CSS を利用しています。

## 技術スタック

- **CETEIcean**: TEI/XMLをHTMLに変換して表示
- **Mirador**: IIIF準拠の画像ビューア
- **HTML/JavaScript**: フレームワークを使用せずに実装

## 使用方法

1. リポジトリをクローン
2. 必要に応じてTEI/XMLファイルを準備
3. ブラウザで`index.html`を開く

## ライセンス

MITライセンス
