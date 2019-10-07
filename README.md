# 開発環境を構築

## ローカル作業準備

リポジトリのクローン

```
git clone {URL}
```

作業ディレクトリへの移動

```
cd picshare-backend
```

## laravel開発環境の構築

ユーザIDを設定

```
export UID=${UID}
```

環境設定ファイルを作成

```
cp src/.env.example src/.env
```

コンテナを起動

```
docker-compose up -d
```

依存するライブラリをインストール

```
docker-compose exec app composer install
```
