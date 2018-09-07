PWSCUP2018 評価用docker環境
===

## 使いかた

### 有用性・安全性評価
1. ローカル環境で、dockerとdocker-composeを使えるようにする
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
1. ローカル環境で、dockerとdocker-composeを使えるようにする
2. 適当な場所で、本レポジトリをcloneする
```bash
$ git clone https://github.com/gghatano/pwscup2018eval
```
3. dataディレクトリに、評価したいA.csv(既に置いてあったら置き換える)と、加工前のトランザクションT.csvを配置する

4. check.bashを実行して、評価する
```bash
$ bash ./check.bash
```
5. 何も表示されなければ、フォーマットはOK。エラーがあれば、行・列番号が表示されるので、修正する

## お問い合わせ
pwscupadmin@pwscup.com
または
https://twitter.com/PWScup_Admin

## ToDo
- スクリプトの内容説明
- 自作評価関数のインターフェース定義と、配置方法の説明
