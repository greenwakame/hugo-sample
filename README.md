## Overview
docker hugo 環境サンプル

## Setup(Docker Compose)
プロジェクト名 : site を作成する
```
docker-compose run -w /usr/share web hugo new site blog
```
フォルダ移動
```
cd site/themes/
```
利用したいテーマをコピーしてくる
```
git clone https://github.com/budparr/gohugo-theme-ananke.git
```
設定ファイルをコピして上書きする
```
cp gohugo-theme-ananke/exampleSite/config.toml ../.
```
フォルダ移動
```
cd ../../
```
起動させる
```
docker-compose up -d
```
下記のURLにアクセス
```
http://localhost:1313
```
新規にページ追加作成するコマンド
```
docker-compose run web hugo new post/page2.md