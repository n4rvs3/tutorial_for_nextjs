## JSXについて

当ディレクトリでは、Next.jsの開発において必須のjsxについて学びます。

まずは以下のコードを見てください。

```
const el = <h1>Hello, JSX</h1>
```

javaScriptを書いたことがある人にとっては違和感を持つコードかもしれません。

こちらは文字列でもなければhtmlでもありません。

これが `jsx` とよばれるJavaScriptの拡張記法です。

座学は[こちら](https://ja.reactjs.org/docs/introducing-jsx.html)を読んでいただくとして、実際に触れてみましょう。

[こちらのコード](./sample.jsx)を見てみましょう。(別窓推奨です)

```
const sample = () => {}
```

こちらの形はアロー関数と呼ばれる記法です。

アロー関数については[MDN アロー関数式](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Functions/Arrow_functions)を参照してください。

基本的にはこの形で記述していきます。

```
const txt = "Hello World"
```

いたって普通のJavaScriptにおける文字列の変数です。

```
return(
  <div>
    <h1>{txt}</h1>
  </div>
)
```

sample関数はhtmlを返します。今回はdivタグに囲まれたh1を返します。

ここで注目すべきは

```
<h1>{txt}</h1>
```

です。ここでは先ほど定義したtxt変数をh1タグの値として記述しています。

本来のhtmlではあり得ない形ですが、jsxはあくまでJavaScriptの拡張でしかないのでこういった記述を行うことができます。

例をあげるとすると事前に中身のない空っぽなhtmlの箱を用意しておき、外部のデータを取得してからその値をhtmlに埋め込むようなことができます。

## まとめ

- jsxはJavaScriptの拡張記法
- htmlに変数を埋め込むことができる

実際はもっと詳しく説明すべき点がありますが、今回はあくまで概要を掴みNext.jsを利用する。といった主旨ですのでこの辺りで[次へ](../React)進みましょう。
