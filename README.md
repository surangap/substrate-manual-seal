# substrate-manual-seal
This skeleton demonstrate the substrate manual seal consensus capability.

## Building
in project root directory, run

```bash
$ cargo build --release
```

## Run Locally

### Run Alice
```bash
$ ./target/release/meta-node --chain=local --alice --base-path=.local/a --port=30334 --ws-port 9944 --ws-external --rpc-cors=all --rpc-methods=Unsafe --rpc-external
```

### Connect to FE
```bash
https://polkadot.js.org/apps/?rpc=ws%3A%2F%2F127.0.0.1%3A9944#/explorer
```

### Trigger to mint a block
```bash
$ curl -H "Content-Type: application/json" -d '{"id":1, "jsonrpc":"2.0", "method": "engine_createBlock", "params": [true, false, null]}' http://localhost:9933/
```
