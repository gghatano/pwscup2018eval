PWSCUP2018 評価用docker環境
===

## 注意
- 正しい動作を保証するものではありませんが，コンテスト参加の手助けとなることを期待して公開します

## 使いかた

### 有用性・安全性評価
1. お手元の環境で、dockerとdocker-composeを使えるようにする
2. 適当な場所で、本レポジトリをcloneする
```bash
$ git clone https://github.com/gghatano/pwscup2018eval
```
3. dataディレクトリに、評価したいA.csv(既に置いてあったら置き換える)とT.csv、R.csvを配置する
4. docker-composeコマンドで、コンテナを起動する
```bash
$ docker-compose up -d
``` 
5. eval.bashを実行して、評価する
```bash
$ bash ./eval.bash 
```
6. data/result.txtに評価結果が保存されるので、内容を確認する

### 提出データのフォーマットチェック
#### 匿名加工データのフォーマットチェック
1. ローカル環境で、dockerとdocker-composeを使えるようにする
2. 適当な場所で、本レポジトリをcloneする
```bash
$ git clone https://github.com/gghatano/pwscup2018eval
```
3. dataディレクトリに、評価したいA.csv(既に置いてあったら置き換える)と、加工前のトランザクションT.csvを配置する

4. check-A.bashを実行して、評価する
```bash
$ bash ./check-A.bash
```
5. 何も表示されなければ、フォーマットはOK。エラーがあれば、行・列番号が表示されるので、修正する
#### 推定対応表のフォーマットチェック
1. ローカル環境で、dockerとdocker-composeを使えるようにする
2. 適当な場所で、本レポジトリをcloneする
```bash
$ git clone https://github.com/gghatano/pwscup2018eval
```
3. dataディレクトリに、評価したい推定対応表F.csvと、推定対象の匿名加工データA.csv、加工前のトランザクションT.csvを配置する(既に置いてあったら置き換える)

4. check-F.bashを実行して、評価する
```bash
$ bash ./check-F.bash
```
5. 何も表示されなければ、フォーマットはOK。エラーがあれば、行番号が表示されるので、修正する

### 評価環境をカスタマイズしたい場合
1. dockerコンテナにログインする
```bash
$ docker-compose exec pwscup2018sample /bin/bash
```

2. /pwscup2018sample/drill/をカスタマイズする

## お問い合わせ
pwscupadmin@pwscup.com
または
https://twitter.com/PWScup_Admin

## ToDo
- スクリプトの内容説明
- 自作評価関数のインターフェース定義と、配置方法の説明
