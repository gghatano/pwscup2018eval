PWSCUP2018 評価用docker環境
===


## 使いかた

- docker, docker-composeをインストールする
- ./data に、R.csvとT.csvを配置する
- コンテナを起動する
```bash
$ docker-compose up -d
``` 
- eval.bashを実行する
```bash
$ bash ./eval.bash 
```
- ./data に、result.txtが出力されるので、内容を確認する
