# dialogue-backend
一問一答アプリのバックエンドリポジトリ

## 開発のススメ方

```shell
# 本リポジトリをcloneする
# コンテナ作成＆起動
docker-compose up -d --build
# コンテナにログイン
docker-compose exec node-dev sh
# コンテナ内でパッケージインストール
npm intall
# コンテナ内でlocalサーバー起動
npm run dev
```

上記を実行した後、以下を実行し、レスポンスが返ってくればOK

```shell
curl -sS localhost:3001/users | jq .
```
レスポンス内容
```json
[
  {
    "id": 1,
    "name": "User1",
    "email": "user1@test.local"
  },
  {
    "id": 2,
    "name": "User2",
    "email": "user2@test.local"
  },
  {
    "id": 3,
    "name": "User3",
    "email": "user3@test.local"
  }
]
```