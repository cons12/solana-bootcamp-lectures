### Environment Setup
1. Install Rust from https://rustup.rs/
2. Install Solana from https://docs.solana.com/cli/install-solana-cli-tools#use-solanas-install-tool

### Build and test for program compiled natively
```
$ cargo build
$ cargo test
```

### Build and test the program compiled for BPF
```
$ cargo build-spf
$ cargo test-spf
```

### Debugging Misc
1. Maintain compatibility of rust with solana
    - `cargo add solana-program@"=2.0.3"` as of 2025March
2. `solana-test-validator` 
    - Spinning up local validator
    - Use `http://127.0.0.1:<port>` as custom RPC URL for https://explorer.solana.com/
3.  For `Cannot find module '@solana/web3.js'` 
    - `npm install --save @solana/web3.js@1`
4. Have enough airdrop, and low enough rent for a successful run
    ```
    solana airdrop 10000
    solana rent 1
    ```