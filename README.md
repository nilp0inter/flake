# nilp0inter/flake: The All-Encompassing Nix Flake

> One flake to rule them all, One flake to find them,
> One flake to bring them all, and in the Nix store bind them.

Welcome to `github.com/nilp0inter/flake`, the all-encompassing Nix flake repository that integrates and manages all my Nix-based configurations. This is the single source of truth for my NixOS hosts, macOS (nix-darwin) machines, nix-on-droid setups, WSL instances, and beyond.

## A Unified Approach with Dendritic Pattern

Building on the power and flexibility of the [Dendritic Pattern](#link-to-dendritic-pattern-source), this repository is structured to:

- Make every Nix file a flake-parts module.
- Enable focused implementation of individual features.
- Support cross-system applicability (NixOS, Home Manager, nix-darwin, etc.).
- Leverage directory paths for intuitive feature categorization.

This organization brings forward a modularity that simplifies managing complexities across:

- Multiple system configurations.
- Shared modules and settings.
- Configuration for different system classes.
- Cross-cutting concerns like theming or common packages.
- Accessing essential values and configurations consistently.

## Core Philosophy & Features

This flake provides a consistent, reproducible, and declarative foundation for all computing environments. Key aspects include:

- **Unified System Configuration:** Define environments for NixOS, nix-darwin, nix-on-droid, and WSL in one place.
- **User Environments:** Manage user-specific packages and settings with Home Manager.
- **Secure Secrets Management:** Use `sops-nix` for encrypting and managing sensitive data.
- **Impermanent Systems:** Implement impermanent filesystems for reproducibility.
- **Declarative Disk Management:** Utilize tools like `disko` for managing disk layouts.
- **Consistent Theming:** Apply `stylix` for a unified visual experience across systems.

## Usage

To interact with this flake for development or inspection:

```console
# Placeholder: Instructions for entering the development shell.
# Example: direnv allow or nix develop
```

## Building & Deploying Systems

This flake defines configurations for various hosts and system types.

### Adding a New Host/System

To incorporate a new system, follow these general steps:

1. **Create a Directory:** [Placeholder for directory structure]
2. **Define Configuration:** [Placeholder for importing modules]
3. **Expose Configuration:** [Placeholder for flake.nix exposure]
4. **Sops-Nix Handling:** If using for the new host, update the host's public key.

```console
# Placeholder: Command or procedure for updating sops keys.
# Example: find ... -exec sops updatekeys -y {} \;
```

### Applying a Configuration

#### NixOS Host:

```console
# Placeholder: Command to build and switch/boot a NixOS configuration.
# Example: inv remote-switch <hostname> <ip>
```

#### macOS (nix-darwin) Host:

```console
# Placeholder: Command to build and switch a nix-darwin configuration.
# Example: darwin-rebuild switch --flake .#<hostname>
```

#### Other Environments:

```console
# Placeholder: Instructions specific to these environments.
```

## System Installation (from scratch)

To provision a new system using a configuration from this flake:

1. **Boot Installer:** [Placeholder for booting instructions]
2. **Connect to Internet:** [Placeholder for connection setup]
3. **Clone Repository:** 
4. **Prepare Disks:** 

```console
# Placeholder: Disk preparation commands using disko or manual steps.
```

5. **Install System:**

```console
# Placeholder: nixos-install command with flake.
# Example: sudo nixos-install --flake .#<hostname> --no-root-passwd
```

## Personal Setup Notes (Post-Installation)

After installation, some manual configurations might be necessary:

- **Repositories:** [Placeholder for `mr update` or equivalent]
- **Gopass:** [Placeholder for `gopass list` testing]
- **Browser Extension:** Manual sync and setup.
- **Syncthing:** Verify shared folder connections.
- **Other Applications:** Specific setup checks.

## Troubleshooting

### Why is a package installed on a host?

Use the following to trace dependencies:

```console
# Placeholder: nix why-depends command.
# Example: nix why-depends .#nixosConfigurations.<H>.pkgs.<P> --derivation
```

## External Hardware How-Tos

### Restore Yubikey OATH tokens

```console
# Placeholder: Yubikey OATH restoration steps.
```

### Restore Timex Datalink 150

```console
# Placeholder: Timex Datalink restoration steps.
```

## Acknowledgements

- The **Dendritic Pattern** concept and its articulation by its developers.
- The `flake-parts` library and its maintainers for simplifying flake composition.
- The Nix community for continuous support and innovation.

<!--
---
Feel free to replace placeholders with specific information as your setup becomes more defined!
-->
