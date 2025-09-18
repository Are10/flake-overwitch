# Nixos Flake for Dagargo's Overwitch
- https://github.com/dagargo/overwitch

This flake builds Overwitch v2.1 from source and installs the required udev rules.

Comes with a devShell.

Based on the nixpkgs work done by https://github.com/dag-h

# Usage:
Include the flake in your `flake.nix`
```
   inputs.overwitch = {
       url = "github:Are10/flake-overwitch/main";
       inputs.nixpkgs.follows = "nixpkgs";
  };

  modules = [
    inputs.overwitch.nixosModules.default
  ];
```

And then enable it in `configuration.nix`
```   
services.overwitch.enable = true; 
```
