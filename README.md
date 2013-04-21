基礎演習手順書
==============

統合開発環境と Git による Web ページ開発
----------------------------------------

HTML の書き方
現在 HTML 5 という規格が策定されている最中で,
主要な Web ブラウザはそれに対応しているものが殆どであるため HTML 5 を前提に演習を行う.

## 1 週目
1 週目の演習では HTML, CSS と Twitter Bootstrap というフレームワークを用いて Web ページを作成する.

### 演習 1. HTML5 のテンプレートから HTML ファイルを作成表示の確認を行う.
[HTML5 テンプレート](template/html5.html "test")

> HTML 5 では、ファイルの先頭の記述が
> ``<!DOCTYPE html>`` に変わっている事に注意する事.
> また、使用する文字のエンコーディングの指定は ``<meta charset="utf-8" />``
> に変更されている事にも注意する.


### 演習 2. CSS の初期化を行う
演習 1 で作成したファイルに CSS 読み込みの記述を行う事.
尚, 以降の演習での編集ファイルは全て同じものを指す.

[CSS 初期化ファイル](template/initialize.css)

> ``<link>`` タグでは外部ファイルから CSS を読み込む事が出来る.
> CSS は, ブラウザ毎に仕様と設定が異なる為, 
> 予期しない動作を引き起こす事がある. 
> その為, あらかじめ設定を初期化して置く事で予期しないレイアウト
> になる事を防ぐ事が出来る.


### 演習 3. Twitter Bootstrap の読み込みを行う.
Bootstrap のダウンロードを行なう.
ファイルは zip 形式で圧縮されている為, 伸長を行い, 適切な場所にファイルを配置する.
ファイルを配出来たなら, ``css/bootstrap.min.css``, ``bootstrap.min.js``
の両ファイルを読み込む事.
下記リンクは Twitter Bootstrap の Official Page である.

[Twitter Bootstrap](http://twitter.github.io/bootstrap/index.html)

> Twitter Bootstrap を読み込む為のテンプレートは Official Page の HTML
> template という項目にサンプルが存在する為, 読み込み方がわからない場合
> は参照する事.


### 演習 4. ナビゲーションバーの作成
Bootstrap を使用し, ナビゲーションバーを作成する.
``css/bootstrap.min.css`` の他に ``css/bootstrap-responsive.css`` を
読み込む. ただし, 読み込む順番は ``bootstrap-responsive.css`` を後に
する. 演習では, ナビゲーションバーはページ最上部へと設置する為,
body タグ内の先頭に記述する.

読み込みの記述後 [ナビゲーションバーサンプル](template/navbar.html) を参考にナビゲーションバーを作成する.

> ナビゲーションバーとは, ユーザーがサイトを巡回する際に,
> コンテンツ毎のアクセスをナビゲートする機能である.
> 複数ページから出来ているサイトの場合はリンクを記述する事が多い.

> 演習 4 にて初めて body 部分の記述を行ったが, 今回の記述で Twitter
> Bootstrap によるレイアウトを行う為には class を使用する事が分かる. 
> その他のページを構成する書式は HTML のままで良い.
> また, 複数の class を組み合わせる事で実装出来るレイアウトもある.

> class に Twitter Bootstrap によって決められた属性を割りあてる
> 事で任意のレイアウトを実装出来るので実際にナビゲーションバーの class
> 属性を削除, 変更して変化を見て置くと理解し易い為推奨する.

### 演習 5. フッターの作成
[フッターサンプル](template/footer.html) を参考にフッターを作成する.
フッターに記述する内容は直接コンテンツに関係のある内容では無い為, 
ページ訪問者から一番目立たない, ページの最下部に記述する. 
その際に style への追記を見落とさない様気を付ける.

> フッターは制作者の情報等を載せる領域である. 
> 連絡先や社名を載せる事が多い.

### 演習 6. コンテンツレイアウト作成
[コンテンツレイアウトサンプル](template/contents.html) を参照し,
コンテンツのレイアウトを作成する. 

> ``class="hero-unit"`` 
> の属性が付いている文書はメインコンテンツ用の色付き且つ, 
> 大領域のレイアウトになる.
> ``class="row"`` 属性の付加された ``class="span4"`` のコンテンツは
> 横並びに出来る.
> また, ``span4`` の数字部分は, 1-9 までの数字を割り当てる事が出来る.
> その場合, コンテンツの領域は数字に合わせて変更される.

## 2 週目
2 週目の演習ではバージョン管理ソフトウェアを用いて Web ページの管理と修正を行う.

### 演習 7. Git リポジトリの作成
Terminal を開き, 作業ディレクトリの最上部に移動する.
その後 ``git init`` を実行する.

> git リポジトリとは Git でソフトウェアを管理する際のデータベースである.
> 演習ではローカル PC に保存する. 

### 演習 8. Git リポジトリへコードを仮登録する
作業ディレクトリ上で ``git add .`` を実行する.

> ``git add`` はリポジトリへの仮登録を行うコマンドである.
> ファイルの更新を行った場合の更新も同様に登録する.
> また, ``.`` はカレントディレクトリを指し示すもので,
> 配下のファイルを全て対象とする.

### 演習 9. Git リポジトリへコミットを行う
作業ディレクトリ上で ``git commit -m "最初のコミット"`` を
実行する. 

> コミットとは, リポジトリに登録したコードや文書を本登録
> する事を指す. 
> また, その際にどの様な変更を行ったかをコメントしておく事が出来る.

### 演習 10. ブランチの作成
作業ディレクトリ上で ``git branch test`` を実行する事でテスト用ブランチを作成出来る.

> 演習 10 では test という名前を用いたが, 本来はどんな名前でも良い.
> その為, その都度適切な名前を付ける事が望ましい.
> ただし, 半角英数字で記述する事.
> ブランチを作成する事によって, ある時点での状態を残す事が出来る.
> 詳しくは演習 11 にて解説する.

### 演習 11. checkout によるリポジトリの状態復元
演習 10 にて作成したブランチにブランチを変更する.
まず, 現在のブランチを確認する為に ``git branch`` を実行する.
その後, ``git checkout test`` を実行し, ブランチを切り替える.
また、切り替えに成功しているかどうかを確認する事.
切り替えに成功している場合は次のような表示がされる.

      master
    * test

ブランチの切り替えの成功が確認出来たら, 作成せいしたページのコードを全て削除する.
コードの削除後にコミットを行い, ページには何も表示されない事を確認する.
尚, コミットメッセージは自由にして良い.

何も表示されない事が確認出来たら ``git checkout master`` を実行し,
ページの状態が, ページのコードを削除する前に復元されている事を確認する.

> ``git checkout`` はブランチの移動を行うコマンドである. 
> Git においてブランチの移動とは, ある時点で記録された状態に
> 戻す事と同義である. また, ブランチの移動を行わない場合でも
> ``git checkout .`` を実行する事で, 一番最近のコミット直後の状態に戻す事が出来る.
> 誤ってファイルを削除した場合や, 変更を加えものの元に戻せない場合に使うと良い.

