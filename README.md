# laravel_project_docker_sample

# Docker での Laravel 開発環境構築

- 2ファイルを配置した後に

```
% docker-compose up -d
```

- Laravel のインストール

```
$ docker-compose exec php composer create-project --prefer-dist "laravel/laravel=8.*" .
```

* composerのメモリ不足エラーが出た場合

```
docker ps でコンテナIDを確認後

% docker exec -it [コンテナID] /bin/sh
```

* コンテナ内でコマンド実行

```
# php -d memory_limit=-1 /usr/bin/composer require --dev 
```

- Laravel 起動

```
 % docker-compose exec php php artisan serve --host=0.0.0.0 --port=8000
```

- http://localhost:8000 にアクセスして動作確認
