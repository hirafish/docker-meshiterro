#　 Readme

## 以前研修で作った[meshiterro](https://github.com/hirafish/meshiterro)を Docker で立ち上げられるようにしました。以下覚書です。

- Dockerfile と docker-compse.yml を加えた(中身コピペ)
- public/packs に manifest.json を追加
- 一旦 lock ファイルの中身を消した(いらないかも)
- エラー通りに Rails のバージョンを合わせた
- yarn と npm を入れたりもした
- config/webpacker.yml の、development の compile を true に書き換えた
