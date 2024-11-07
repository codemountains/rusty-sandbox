# Sandbox for Rust on Dev Container

A Rust development environment that runs on Dev Container.

> [!IMPORTANT]
> This setup has been verified to work with Visual Studio Code.

## Visual Studio Code Setup

Install the [Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension for [Visual Studio Code](https://code.visualstudio.com/).

Additionally, install [Docker](https://docker.com/) in your local environment.

## Developing with Rust

### Running

Verify that Rust and Cargo are installed:

```shell
rustc --version
cargo --version
```

Try outputting "Hello, world!":

```shell
cargo run
```

### Adding a New Crate

Execute the `cargo new` command:

```shell
cargo new NEW_CRATE_NAME
```

Verify that the newly added crate is listed in the `members` section of `Cargo.toml`:

```toml
members = [
    "app",
    "NEW_CRATE_NAME"
]
```

Run the specific package using the `--package` option:

```shell
cargo run --package NEW_CRATE_NAME
```

## License

This project is licensed under the [MIT license](LICENSE).
