# devcon-node-dod-git

これは、mcr.microsoft.com/devcontainers/typescript-node:14-bullseye の Dev Container をベースとして、下記 features を追加したイメージ devcon-node-dod-git をビルドするためのリポジトリです。

- ghcr.io/devcontainers/features/docker-outside-of-docker
- ghcr.io/devcontainers/features/git
- ghcr.io/devcontainers/features/git-lfs

node ユーザーを使うことを想定していて、Docker ボリュームで `/home/node/workspace` をマウントしやすくしています。また、下記もインストールしています。

- bash-completion

実行するには、Linux で実行可能な Node.js の環境が必要です。下記のようにコマンドを実行することで devcon-node-dod-git:1.0 の Docker イメージを作成することができます。

```console
sh build.sh
```
