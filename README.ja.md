# Sandbox for Rust on Dev Container

Dev Container で動作する Rust の開発環境です。

> [!IMPORTANT]
> Visual Studio Code で動作確認をしています。

## Visual Studio Code セットアップ

[Visual Studio Code](https://code.visualstudio.com/) に拡張機能 [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) をインストールします。

また、ローカル環境に [Docker](https://docker.com/) をインストールします。

## Rust で開発する

### 実行

Rust や Cargo がインストールされていることを確認します。

```shell
rustc --version
cargo --version
```

`"Hello, world!` を出力してみます。

```shell
cargo run
```

### 新しいクレートを追加する

`cargo new` コマンドを実行します。

```shell
cargo new NEW_CRATE_NAME
```

`Cargo.toml` の `members` に新しく追加したクレートがあることを確認します。

```toml
members = [
    "app",
    "NEW_CRATE_NAME"
]
```

`--package` オプションでパッケージ名を指定して実行します。

```shell
cargo run --package NEW_CRATE_NAME
```

## License

This project is licensed under the [MIT license](LICENSE).
