# install-scripts

User-directory install scripts for Linux applications that don't offer native packages for every distro. Everything goes under `~/.local/` — no root required.

## Scripts

### Free Download Manager

Installs [Free Download Manager](https://www.freedownloadmanager.org/) by extracting the official `.deb` package into `~/.local/`.

**Install:**

```bash
curl -fsSL https://raw.githubusercontent.com/fhsinchy/install-scripts/master/install-fdm.sh | bash
```

**Uninstall:**

```bash
curl -fsSL https://raw.githubusercontent.com/fhsinchy/install-scripts/master/install-fdm.sh | bash -s -- --uninstall
```

**What it does:**

- Downloads and extracts the official FDM `.deb` (no `dpkg` needed)
- Installs the app to `~/.local/opt/freedownloadmanager/`
- Creates a wrapper at `~/.local/bin/fdm` with the correct `LD_LIBRARY_PATH`
- Adds a `.desktop` file and SVG icon for app menu integration
- Registers the native messaging host for browser extension support (Chrome, Chromium, Brave, Edge, Vivaldi, Opera)
- Idempotent — re-run to update

**Requirements:**

- x86_64 Linux (any distro)
- `ar`, `tar`, and `curl` or `wget`
- `~/.local/bin` in your `PATH`

## License

MIT
