# Docker_laravel
このリポジトリはssh接続のテスト用のリポジトリですでした。
ssh接続がうまくいったので次はララベルの環境構築をdockerを用いて行うリポジトリになりました。

ctrl + shift + vでプレビューを確認してください

# Docker 環境構築

### 0. 前提条件
- Dockerがインストールされている(`docker -v`で確認できるよ)


### 1. ディレクトリ構造の決定
- wsl2のインストール

    管理者権限でコマンドプロンプトを開き、下記コマンドで状態確認

    `wsl --status`

    レスポンスとして
    ```
    既定のディストリビューション: Ubuntu
    既定のバージョン: 2
    ```

    となっていればok

    それ以外の場合は下記コマンドでwslをインストール

    `wsl --install`


### 2. Apacheコンテナの構築

### 3. Apacheコンテナの構築

### Docker 注意点

WindowsでDockerを使う際正しくファイルを配置しないと激重になるので注意してください

参考 : [WindowsでのDocker注意点](https://qiita.com/minato-naka/items/84508472c04f628e576e)

# Docker基本コマンド
```
########イメージの操作########
#イメージ一覧を表示
docker images

#Docker Hubからイメージを取得
docker pull {イメージ名}

#Dockerfileからイメージを作成
docker build {Dockerfileのパス}

#イメージを削除
docker rmi {イメージID}


########コンテナの操作########
#コンテナ一覧を表示
docker ps -a

#コンテナを作成
docker create {イメージ名}

#コンテナを起動
docker start {コンテナ名} 

#コンテナを停止
docker stop {コンテナ名}

#コンテナを削除
docker rm {コンテナ名} 

#イメージを取得、コンテナを作成、コンテナを起動
docker run {イメージ名}


########その他の操作########
#コンテナにログイン
docker exec -it {コンテナ名} bash
```

# 参考
- [基本的な書き方とフォーマットの構文](https://docs.github.com/ja/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

- [Laravel Sail エイリアスの設定方法](https://qiita.com/tomo332/items/f6c8c1b4fbcf1d828940)

- [Laravel 環境構築](https://qiita.com/minato-naka/items/8b31d28823cabaa9487a)