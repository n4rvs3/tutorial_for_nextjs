# Install Node.js

当ディレクトリでは、`Node.js` のインストールを行います。

既にインストール済みの方は[次の項目](../jsx)に進んでください。

## Node.jsとは

本来JavaScriptはブラウザ上にて動作するプログラミング言語です。

ブラウザ上で動作するJavaScriptはOS上の機能対して限定的なアクセス権限しか持ちません。(カメラやマイク等に対してのアクセス)

そこで、OS上の機能を利用できるように開発されたのが`Node.js`です。

Node.jsを用いることでOS上の機能にアクセスするプログラムをJavaScriptで開発することができます。

Node.jsは前提としてWebサーバでもなければフレームワークでもなく、単純なJavaScript実行環境です。

ただ、現在ではNode.jsはサーバサイドとクライアントサイド(ブラウザ)両方のJavaScript実行環境として利用されています。

[Node.jsとは](https://nodejs.org/ja/about/)

[Node.jsとはなにか？](https://qiita.com/non_cal/items/a8fee0b7ad96e67713eb)

## インストール方法

座学は置いておいて、実際にインストールを行います。

Node.jsのインストール方法は様々な方法がありますが、今回は `nodenv` を用いたインストールを行います。

Windowsをお使いの方は `Volta` をお勧めします。

<details><summary>macOS</summary>

Homebrewがインストール済み前提です。

もしインストールしていない場合は

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

を実行してください。

では、nodenvをインストールしてきます。

```
brew install nodenv
```

を実行してください。

次に、パスを通します。

お使いのターミナルウィンドウの一番上に「bash」や「zsh」等の記載があると思います。そこに記載の名前によって書き込むファイルが変わります。

<details><summary>zshの場合</summary>

```
echo eval "$(nodenv init -)" >> ~/.zshrc
```

と実行してください。

</details>

<details><summary>bashの場合</summary>

```
echo eval "$(nodenv init -)" >> ~/.bash_profile
```

と実行してください。

</details>
<br />

実行しましたら一度ターミナルを再起動し

```
curl -fsSL https://github.com/nodenv/nodenv-installer/raw/master/bin/nodenv-doctor | bash
```

を実行してください。エラーが表示されない場合は次へ進みます。

```
nodenv -v
```

を実行するとバージョンが表示されます。

これでnode.jsのインストールをする準備が整いました。ではインストールしていきましょう。

```
nodenv install 16.16.0
↓
nodenv rehash
↓
nodenv global 16.16.0
```

実行すると、執筆時での安定版(v16.16.0)をインストールできました。

インストールするバージョンに関しては適時公式サイトにて安定版を確認、変更してください。

```
node -v

↓

v16.16.0
```

と表示されるのを確認し、完了です。お疲れ様でした！

</details>
