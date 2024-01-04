# devcon-node-dod-git

これは、[mcr.microsoft.com/devcontainers（0.3.26）の typescript-node:18-bookworm](https://github.com/devcontainers/images/tree/v0.3.26/src/typescript-node) の Dev Container をベースとして、下記 features を追加したイメージ devcon-node-dod-git をビルドするためのリポジトリです。

- ghcr.io/devcontainers/features/docker-outside-of-docker
- ghcr.io/devcontainers/features/git
- ghcr.io/devcontainers/features/git-lfs

node ユーザーを使うことを想定していて、Docker ボリュームで `/home/node/workspace` をマウントしやすくしています。また、下記もインストールしています。

- bash-completion

実行するには、Linux で実行可能な Node.js の環境が必要です。下記のようにコマンドを実行することで devcon-node-dod-git:1.18 の Docker イメージを作成することができます。

```console
sh build.sh
```

## ディレクトリ構成について

ディレクトリ構成は次のようになっています。

```text
./
├── .devcontainer/ ... 開発コンテナのビルド用ファイル
│   ├── Dockerfile
│   └── devcontainer.json
├── LICENSE ... ライセンス
├── README.md ... このファイル
├── build.sh ... ビルド用スクリプト
└── dev/ ... 開発時に使用するものを管理するためのディレクトリ
    └── docker-compose.yml
```
