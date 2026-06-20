<p align="center"><img src="https://raw.githubusercontent.com/go-quake3/brand/main/social/go-quake3.png" alt="go-quake3/go-quake3.github.io" width="720"></p>

# go-quake3.github.io

Sources for **go-quake3.github.io** — the go-quake3 family landing page.
Built by [Hugo](https://gohugo.io) — same toolchain and same template
shape as [go-tpm2.github.io](https://github.com/go-tpm2/go-tpm2.github.io)
and [go-virtio.github.io](https://github.com/go-virtio/go-virtio.github.io).
Brick-red palette so it reads as a Quake-family page.

## Layout

```text
.
├── hugo.toml                       Site config + per-repo card params
├── content/
│   └── _index.md                   Homepage marker (empty)
├── layouts/
│   └── index.html                  Homepage body (inline CSS + theme toggle)
├── static/
│   ├── favicon.svg                 Org logo, used as favicon
│   └── img/logo.svg                Org logo, used as hero (88px)
└── public/                         Hugo build output (gitignored — built by CI)
```

## Build locally

```sh
hugo server -D                            # live reload at http://localhost:1313/
hugo --gc --minify                        # production build → ./public/
```

## Deploy

`.github/workflows/hugo.yml` builds + deploys on every push to `main`.
Configure GitHub Pages on the repo with **Source = "GitHub Actions"**
(not "Deploy from a branch").

## Sibling pages

- [go-quake2](https://go-quake2.github.io) — id Tech 2 (1997), reserved.
- [go-quake3](https://go-quake3.github.io) — id Tech 3 (1999), reserved.
- [cloud-boot](https://cloud-boot.github.io) — the UEFI bootloader that
  hands control to the TamaGo Quake guest.
- [godoom](https://github.com/cloud-boot/godoom) — sibling DOOM port; same
  4-gate provable-test protocol.
