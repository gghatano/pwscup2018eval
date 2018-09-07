PWSCUP2018 評価用docker環境
===

## 使いかた

1. ローカル環境で、dockerとdocker-composeを使えるようにする
2. 適当な場所で、本レポジトリをcloneする
```bash
$ git clone https://github.com/gghatano/pwscup2018eval
```
3. dataディレクトリに、評価したいA.csvとR.csvを配置する(既に未加工のT.csvが配置してあるので、置き換える)
4. docker-composeコマンドで、コンテナを起動する
```bash
$ docker-compose up -d
``` 
5. eval.bashを実行して、評価する
```bash
$ bash ./eval.bash 
```
6. data/result.txtに評価結果が保存されるので、内容を確認する

## お問い合わせ
pwscupadmin@pwscup.com
または
https://twitter.com/PWScup_Admin

## ToDo

- フォーマットチェッカの動作環境作成
