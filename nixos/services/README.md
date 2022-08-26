# Building Binaries 
### Buidling Solana
```
# enter the solana shell
nix-shell solana-shell.nix

rustup default stable 
cd solana
cargo build --release
```
### Building `prometheus_account_exporter`
```
cd prometheus_acccount_exporter
nix-shell -p cargo libiconv openssl pkgconfig --run "cargo build --release --example solana --features=hyper_server"
```
