Back-up
```
cd ~/nixos
git pull --rebase
cp /etc/nixos/configuration.nix ~/nixos/
git add configuration.nix
git commit -m "Update NixOS configuration"
git push
```

Edit
```
sudo nano /etc/nixos/configuration.nix
```

Rebuild and test
```
sudo nixos-rebuild test
```

Rebuild and switch
```
sudo nixos-rebuild switch
```

Rebuild and boot
```
sudo nixos-rebuild boot
```

Rollback
```
sudo nixos-rebuild switch --rollback
```

Rebuild and upgrade
```
sudo nixos-rebuild switch --upgrade
```

List generations
```
sudo nixos-rebuild list-generations
```

Delete older generations
```
sudo nix-collect-garbage --delete-older-than 30d
```

Temporary install packages
```
nix-shell -p <package>
```

Aggressive cleanup
```
sudo nix-collect-garbage -d
sudo nix-store --optimise
```
