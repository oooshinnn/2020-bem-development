ブログ記事 [実践BEM 〜開発環境の構築〜 | oshin.tokyo](https://oshin.tokyo/entry/2020-bem-development) の中で紹介する開発環境のサンプルコードです。

# 使い方

macOSを前提に説明します。

npm scriptsの実行の仕方がわかる、という方は説明を読むことなく環境が利用できると思いますので、そうではない方向けに順を追って説明します。

## Node.jsが使える状態にする

Macのデフォルトアプリ「ターミナル」を開き、`$ `に続いて`node -v`と入力し、Enterを押します。

`v11.14.0` などとインストールされているバージョンが表示されればすでにNode.jsが使える状態です。

バージョンが表示されなかった場合は、[Node.js公式サイト](https://nodejs.org/ja/)からインストーラーをダウンロードし、インストールしてください。

Node.jsが使える状態になっていれば、同時に`npm`コマンドも使えるようになるはずです。念のためターミナルで`npm -v`と入力してバージョンが表示されるか確認しておくと良いでしょう。


## リポジトリをダウンロードする

※ gitコマンド、またはSourceTreeなどのgitクライアントを使ってリポジトリのクローンができる方は好きな方法でクローンしていただいて構いません。

この画面の右上にあるボタン「Clone or download」をクリックし、表示されたメニューから「Download ZIP」をクリックすると、この環境全体がダウンロードされます。「2020-bem-development-master」といった名前のzipファイルになるかと思います。

それを好きな場所に展開してください。


## 必要なパッケージのインストール

先ほどダウンロードし展開したフォルダーをターミナルで開きます。

ターミナルアプリを開き、`$ `に続いて`cd `と入力した後、ダウンロードしたフォルダーをターミナルの上にドラッグアンドドロップします。`cd `の後に、ダウンロードしたフォルダーのパスが入力されたことを確認し、Enterを押します。

これで、フォルダーの場所に移動できました。確認のため`$ `に続いて`pwd`と入力しEnterを押し、表示された場所の末尾が`/2020-bem-development-master`となっていることを確認します。

ここで、必要なパッケージのインストールを行います。

`$ `に続いて`npm install`と入力しEnterを押します。少しの時間インストールが続き、エラーなく（ERRORといった表示や赤い文字などが表示されることが多いです）、再び`$ `が表示されればインストール完了です。

ダウンロードしたフォルダーの中に、node_modulesというフォルダーが追加されていればOKです。

## ビルドの実行

`npm install`を実行したのと同じ場所で、`$ `に続いて`npm run dev`と入力しEnterを押します。いろいろと自動で処理が走り、buildというフォルダーが追加されていれば完了です。



# 構成

## `/src`

コンパイル元のpug、sassが入っています。

## `/build`

`/src`フォルダーの内容をコンパイルした結果が入ります。このフォルダーは自動で生成・更新されます。