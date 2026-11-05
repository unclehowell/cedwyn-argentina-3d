# Argentina Tŷ Mawr 3D world

The Argentina Tŷ Mawr 3D world webapp of [cedwyn.bucklerfamily.estate](https://cedwyn.bucklerfamily.estate/argentina/), in its own repository.

It was split out of `unclehowell/cedwyn` (branch `section/argentina-3d`) on 5 Nov 2026, because that repository holds about 290 branches
(~43 GB with history) and a job on one webapp should never need the rest. This repository is a few MB
(12 files, 0.2 MB at the split).

## Get the code

```
git clone --depth 1 https://github.com/unclehowell/cedwyn-argentina-3d.git
```

## Where to send changes (read this first)

`split-repos.json` on `unclehowell/cedwyn` main sets the mode:

- **mirror** (now): the old branch `section/argentina-3d` on unclehowell/cedwyn is still the source. `mirror.yml` here copies it every
  30 minutes. Send pull requests to `section/argentina-3d` on unclehowell/cedwyn (clone it with
  `git clone --depth 1 --single-branch --branch section/argentina-3d --filter=blob:none https://github.com/unclehowell/cedwyn.git`).
- **split-repo** (after the owner switches it): this repository is the source; send pull requests here.
  unclehowell/cedwyn copies `main` back into `section/argentina-3d`, so the live page and every old path keep working.

`SPLIT.json` records the source commit of the last copy. The app's own notes, if the branch had any, are in `APP-README.md`.

## Previews

`preview.yml` deploys every pull request to Cloudflare Pages and comments the link, once the repository secrets
`CLOUDFLARE_API_TOKEN` and `CLOUDFLARE_ACCOUNT_ID` are set (Settings → Secrets → Actions). Without them it stops quietly.

## History before the split

The full history stays on the old branch: https://github.com/unclehowell/cedwyn/commits/section/argentina-3d

Latest commits on `section/argentina-3d` at the split:

| Date | Commit | Change |
| --- | --- | --- |
| 2026-11-05 | `0359f8a` | section/argentina-3d: note the Cloudflare staging preview URL in README |
| 2026-11-04 | `8d97ea5` | Argentina 3D v0.2.0: frame the helicopter view closer on phones |
| 2026-11-04 | `4f148f9` | Argentina 3D v0.2.0: changelog |
| 2026-11-04 | `2e65beb` | Argentina 3D v0.2.0: Tŷ Mawr rebuilt from three reference photographs, helicopter and ground views |
| 2026-11-04 | `b36e8de` | argentina-3d v0.1.0: stone and lime-wash textures cut from album photograph 098 |
| 2026-11-04 | `c8a7f9b` | argentina-3d v0.1.0: sky shader (three r160), README, changelog |
| 2026-11-04 | `3aaa5de` | argentina-3d v0.1.0: separate Patagonia 3D world with Tŷ Mawr reconstructed from the 1974 survey and album pho |

Never force-push; never delete the old branch.
