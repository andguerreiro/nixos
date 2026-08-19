Back-up
```
cp /etc/nixos/configuration.nix ~/nixos/
cd ~/nixos
git add .
git commit -m "Update NixOS configuration"
git push
```

Clear
```
sudo nix-collect-garbage -d
sudo nix-store --optimise
```
