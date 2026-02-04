# install-scripts

User-directory install scripts for Linux applications that don't offer native packages for every distro. Everything goes under `~/.local/` — no root required, distro agnostic.

## Usage

Each script supports `--uninstall` to cleanly remove everything it installed. Re-running a script updates the existing installation.

Make sure `~/.local/bin` is in your `PATH`:

```bash
export PATH="$HOME/.local/bin:$PATH"
```

## Available scripts

| App | Install | Uninstall |
|-----|---------|-----------|
| [Free Download Manager](https://www.freedownloadmanager.org/) | `curl -fsSL https://raw.githubusercontent.com/fhsinchy/install-scripts/master/install-fdm.sh \| bash` | `curl -fsSL https://raw.githubusercontent.com/fhsinchy/install-scripts/master/install-fdm.sh \| bash -s -- --uninstall` |

## License

MIT
