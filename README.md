# RickRollOS
A small kernel written in rust, that rickrolls the user upon boot, built upon this tutorial: https://os.phil-opp.com/

To run it on linux with QEMU, or just a .bin file:
```
rustup target add thumbv7em-none-eabihf
rustup override add nightly.
cargo install cargo-xbuild
cargo install bootimage
rustup component add llvm-tools-preview
cargo bootimage
qemu-system-x86_64 -drive format=raw,file=target/x86_64-blog_os/debug/bootimage-os.bin
```
