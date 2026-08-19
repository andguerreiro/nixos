Back-up
```
cp /etc/nixos/configuration.nix ~/nixos/
cd ~/nixos
git pull --rebase
git add .
git commit -m "Update NixOS configuration"
git push
```

Clear
```
sudo nix-collect-garbage -d
sudo nix-store --optimise
```

Usefull
```
sudo nano /etc/nixos/configuration.nix
```
```
sudo nixos-rebuild switch
```
```
sudo nixos-rebuild boot
```
```
sudo nixos-rebuild switch --upgrade
```
```
sudo nix-env --list-generations --profile /nix/var/nix/profiles/system
```
```
nix-shell -p <package>
```
