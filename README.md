### kunaiがサポート終了するとのことで我々が新しく作るのだ
## 参考文献
### Flutter×Firebaseでdocker環境の構築を行う
https://qiita.com/shunn0818/items/088e46bc180dc474641e


## 環境構築
dockerでflutterの開発環境を構築する

## dockerのビルド
```
docker-compose build
```

## dockerのコンテナを構築、起動
```
docker-compose up -d
```

## 起動したコンテナに入る
```
docker exec -it flutter bash
```

## Flutterでのプロジェクト作成
```
cd ${APP_CODE_PATH_CONTAINER}
flutter create .
```
## Dockerコンテナ内でFlutterプロジェクトを実行
# サーバーを起動します。
Dockerコンテナ内でFlutterプロジェクトを実行し、開発プロセスを効率化する方法を説明します。

サーバーを起動します。
```
flutter run -d web-server --web-port=${WEB_SERVER_PORT} --web-hostname 0.0.0.0
```