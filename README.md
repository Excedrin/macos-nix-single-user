# macos-nix-single-user

```
curl -L https://nixos.org/nix/install | sed 's/^"$script/#"$script/; s/unpack=$tmpDir\/unpack/unpack=nix\/unpack/' > get-nix-installer
./get-nix-installer
patch -i single-user.patch
./nix/unpack/nix-2.25.2-aarch64-darwin/install --no-daemon
```
