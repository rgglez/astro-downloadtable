# astro-downloadtable

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
![GitHub all releases](https://img.shields.io/github/downloads/rgglez/astro-downloadtable/total)
![GitHub issues](https://img.shields.io/github/issues/rgglez/astro-downloadtable)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/rgglez/astro-downloadtable)
[![GitHub release](https://img.shields.io/github/release/rgglez/astro-downloadtable.svg)](https://github.com/rgglez/astro-downloadtable/releases/)
![GitHub stars](https://img.shields.io/github/stars/rgglez/astro-downloadtable?style=social)
![GitHub forks](https://img.shields.io/github/forks/rgglez/astro-downloadtable?style=social)

**astro-downloadtable** allows users to download a table wrapped with this
component as a CSV file.

One use case is a blog post (Markdown or MDX), where you can download a table
directly from the page.

![Example screen](example_screen.png)

## Installation

```bash
npm install @rgglez/astro-downloadtable
```

## Usage

Import the component:

```mdx
import downloadtable from "@/components/downloadtable.astro";
```

Wrap a checklist with the component in your MD/MDX files:

```mdx
<DownloadTable filename="2fa-inventory.csv" label="Download">
| Service | Username/email | 2FA active | Method | Second device | Backup codes | Last test | Notes |
|---|---|---:|---|---|---|---|---|
| Google | user@example.com | yes | TOTP/passkey | yes | yes | 2026-05-10 | Critical account |
| GitHub | user | yes | TOTP/FIDO2 | yes | yes | 2026-05-10 | Private repos |
| Cloudflare | user@example.com | yes | TOTP/FIDO2 | yes | yes | 2026-05-10 | Domain DNS |
</DownloadTable>
```

Now, when you view the rendered MDX or Markdown in the browser, you'll see a
download button. Clicking it will download the checklist in CSV format.

### Properties

| Name | Value |
|------|------|
| `filename` | The default name of the file to download |
| `label` | The text for the download button (Default: "Download checklist") |

## Development

| Target | Description |
|--------|-------------|
| `make tags` | List git tags sorted by semver (descending) |
| `make latest-tag` | Show the latest git tag |
| `make patch` | Bump PATCH version in `package.json`, commit, tag, and push |
| `make publish` | Publish current version to npm |

Typical release flow: `make patch publish`.

## License

Copyright (C) 2026 Rodolfo González González.

Licensed under the
[Apache v2.0](https://www.apache.org/licenses/LICENSE-2.0.txt). Read the
[LICENSE](LICENSE) file.
