# Almanac
Config Management For Chia Farmers

<p align="center">
    <img src="https://user-images.githubusercontent.com/8990544/225270503-48f90e4e-3e40-4905-bd7c-28354bdb47a5.png">
</p>

Chia configuration is stored in `~/.chia/mainnet/config/config.yaml`. However, with each Chia release, configuration entries may be added, removed, or changed, and Chia doesn't offer a built-in way to maintain your existing `config.yaml` file through updates. That's where `almanac` comes in.

`almanac` helps you keep your `config.yaml` up-to-date and in sync with Chia's expected configuration options. To use `almanac`, execute it in the root directory of your freshly updated `chia-blockchain` project.

### Usage

1. Add `almanac` to your `PATH`.
2. `cd` to your `chia-blockchain` repo.
3. Run `almanac`.

`almanac` compares your current `config.yaml` with the reference `initial-config.yaml` file from the latest commit of your `chia-blockchain` repo.

### Requirements

- `pyaml`: Install with `pip install pyaml`.
- `yq`: Get it here https://github.com/mikefarah/yq/#install

### Customization

`almanac` opens the diff view using the application specified in the `DIFFTOOL` environment variable, defaulting to `vimdiff` if not set. To use a different tool, like `meld`, run `DIFFTOOL=meld almanac`, or export the variable before running.

https://user-images.githubusercontent.com/8990544/157250270-79909a1a-e5bd-42cf-bef4-23c771716fbf.mp4
