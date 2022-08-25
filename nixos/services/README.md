# Building Binaries 
### Buidling Solana
```
cd solana
nix-shell -p cargo libiconv openssl pkgconfig protobuf3_11 udev clang --run "cargo build --release"
```
### Building `prometheus_account_exporter`
```
cd prometheus_acccount_exporter
nix-shell -p cargo libiconv openssl pkgconfig --run "cargo build --release --example solana --features=hyper_server"
```
