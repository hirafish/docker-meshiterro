# Readme

## 以前研修で作った[meshiterro](https://github.com/hirafish/meshiterro)を Docker で立ち上げられるようにしました。以下覚書です。

- Dockerfile と docker-compse.yml を加えた(中身コピペ)
- public/packs に manifest.json を追加
- 一旦 lock ファイルの中身を消した(いらないかも)
- エラー通りに Rails のバージョンを合わせた
- yarn と npm を入れたりもした
- config/webpacker.yml の、development の compile を true に書き換えた

起動方法

```powershell
docker-compose build
docker-compose run web rails db:create
docker-compose up
```

した後に、別のターミナルを起動して(上手くいかなかったら動かしてる docker ファイルディレクトリまで移動)

```powershell
docker-compose exec web bash
```

すると入れる！場合によっては
bin/rails db:migrate rails_env=development
のエラーが http://localhost:3000/ で出ているので、そこで
bin まで移動してから

```powershell
rails db:migrate rails_env=development
```
