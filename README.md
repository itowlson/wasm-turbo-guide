# wasm-turbo-guide

A WASM hello-world with a publish action

You will need:
* Rust: https://www.rust-lang.org/tools/install
* The `wasm32-wasi` target: `rustup target add wasm32-wasi`

To build:
* VS Code: `Run Task > Rust: Build WASM`
* Command line: `cargo build-wasm`

To run:
* VS Code: go to Run/Debug pane, select `Debug WASM` and run
* Command line: `wasmtime ./target/wasm32-wasi/debug/wasm-turbo-guide.wasm`


## Dev releases

* **You will need the Hippo uploader to publish dev builds.** Download this from
  https://github.com/deislabs/hippofactory/releases and install on your path.

## CI releases

The release workflow depends on one variable and two secrets:

* **BINDLE_URL** (defined in .github/workflows/release.yml): the
  URL of the Bindle server where you'd like to
  publish releases. We've set this up for you.
* **BINDLE_USER_ID** (secret you need to create in GitHub): the ID
  of a user with push access to the Bindle server.
* **BINDLE_PASSWORD** (secret you need to create in GitHub): the
  password of the user identified in BINDLE_USER_ID.

See https://bit.ly/2ZqS3cB for more information about creating the
secrets in your GitHub repository.
