PWSCUP2018 評価用docker環境
===


## 使いかた

- ローカル環境で、dockerとdocker-composeを使えるようにする
- 適当な場所で、本レポジトリをcloneする
```bash
$ git clone https://github.com/gghatano/pwscup2018eval
```
- ./data に、評価に利用するR.csvとT.csvを配置する
- docker-composeコマンドで、コンテナを起動する
```bash
$ docker-compose up -d
``` 
- eval.bashを実行する
```bash
$ bash ./eval.bash 
```
- ./data に、result.txtが出力されるので、内容を確認する
