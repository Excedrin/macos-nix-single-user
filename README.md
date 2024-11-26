# macos-nix-single-user

Based on this:
https://ianthehenry.com/posts/how-to-learn-nix/installing-nix-on-macos/

```
curl -L https://nixos.org/nix/install | sed 's/^"$script/#"$script/; s/unpack=$tmpDir\/unpack/unpack=nix\/unpack/' > get-nix-installer
./get-nix-installer
patch -i single-user.patch
./nix/unpack/nix-2.25.2-aarch64-darwin/install --no-daemon
```

Also, I don't actually use this, I (strongly) prefer multi-user install, but this seems to work fine.
