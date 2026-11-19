# SP Baojun — support & releases

The public site for the **SP Baojun** software, served by GitHub Pages at
**https://dsokpheang.github.io/sp_baojun_support/**.

> Nothing private lives here — no keys, no keystores, no research notes. Those stay in
> the private `sp_baojun` repo. `.gitignore` carries guard rules for that reason.

| Path | What |
|---|---|
| `index.html` | Landing page |
| `support/index.html`, `support/privacy.html` | Support + privacy |
| `assets/` | `site.css` (shared look with sp_avatr_support) + the Kit's icon at 180/96/32/16 |
| `sp_suites/` | Release folder: one APK per app + `index.json` (package, version, size, **SHA-256**) |
| `.nojekyll` | Load-bearing: stops Pages from reinterpreting `sp_suites/` |

**Never edit `sp_suites/` by hand** and **never rename it** — SP Baojun Kit on every car reads
`sp_suites/index.json` from this repo. Publish from the private repo:

```sh
cd ~/development/sp_baojun
python3 tools/publish_support_site.py ~/development/sp_baojun_support --push
```

Pages settings: deploy from branch `main`, folder `/`. No build step.

---
© 2026 Sokpheang Duong. All rights reserved. See [LICENSE](LICENSE).
