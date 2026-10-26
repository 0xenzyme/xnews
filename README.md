# 船长 · X AI 新闻 / Captain · X AI News

MkDocs Material site for high-signal AI intel from X. Daily digest plus Chinese and English topic briefs, aimed at builders.

- Live (after merge + first Actions run): https://xnews.0xenzyme.dev/
- Repo: https://github.com/0xenzyme/xnews
- Social: [X @enzyme_dev](https://x.com/enzyme_dev)

Deployed to GitHub Pages by `.github/workflows/deploy.yml` on every push to `main`.

## Enable GitHub Pages

If the first deploy job sits on Pages permissions, set **Settings → Pages → Source = GitHub Actions** (not “Deploy from a branch”). The workflow uploads the `site/` artifact and deploys it.

## Layout

- `docs/{Daily,Chinese-Topics,English-Topics}/*.md` — reports (YAML frontmatter `title`, `type`, `date`, `tags`, `source`, `window`, `generated`, `coverage`; else first `#` heading / filename date).
- `hooks/autonav.py` — at build time generates nav, each category `index.md` and the homepage (newest first). Never edit `mkdocs.yml` to add reports. Generated `index.md` files are overwritten at build; don't hand-edit them.
- `hooks/presentation.py` — homepage pitch, report fact rows, label styling, CSS/JS cache-bust. It does not modify report sources. Design lives in `docs/stylesheets/extra.css`.

There is no email / Substack subscribe CTA. The site is the product.

## Grok Bot box layout

On the bot box the publish path is two directories plus `sync.sh`:

| Path | Role |
|------|------|
| `/workspace/News/{Daily,Chinese-Topics,English-Topics}/` | Bot **writes** reports here (source) |
| `/workspace/news-site/` | git clone of `0xenzyme/xnews` (publish target) |
| `/workspace/news-site/sync.sh` | mirrors Markdown into `docs/`, commits, pushes `main` |

```sh
gh repo clone 0xenzyme/xnews /workspace/news-site
cd /workspace/news-site && gh auth setup-git
mkdir -p /workspace/News/{Daily,Chinese-Topics,English-Topics}
```

`sync.sh` uses `SRC=/workspace/News` and `REPO=/workspace/news-site`. It pulls, mirrors add/update/delete of `*.md` (keeps generated `index.md` / `index.en.md`), commits `sync reports YYYY-MM-DD HH:MM` when something changed, and pushes `origin main`. Watch the Pages run with:

```sh
gh run list -R 0xenzyme/xnews
gh run watch -R 0xenzyme/xnews
```

## Markdown contract

Hooks only parse; they do not write report bodies.

**Frontmatter keys:** `title`, `type`, `date`, `tags`, `source`, `window`, `generated`, `coverage`.

| Category | `type` | Body shape |
|----------|--------|------------|
| `Daily/` | `x-news-daily` | `#` title, `##` sections, `###` items with 发生了什么 / 为什么值得关注 / 原帖与互动 / 核验 / 判断 (EN: What happened / Why it matters / Original post & engagement / Verification / Take) |
| `Chinese-Topics/` | `x-cn-topic-brief` | `## 今日必读` + `## 更多话题` cards |
| `English-Topics/` | `x-en-topic-brief` | `## Today's must-reads` (zh twin: 今日必读) + More topics cards |

Filenames: `YYYY-MM-DD-<slug>.md` plus a same-stem `.en.md` twin. Verification labels: `verified` / `author-claim` / `unverified`.

The `2026-10-21-*` files in this repo are **fake scaffold placeholders** used to prove the build. Do not treat them as real intel.

## Local validation

```sh
pip install -r requirements.txt
mkdocs build
```

The build regenerates tracked index files. Do not include unrelated generated index changes in presentation-only commits.

## Bilingual (中文 / English)

- Plugin `mkdocs-static-i18n` (suffix layout): `foo.md` = Chinese (default, served at `/`), `foo.en.md` = English (served at `/en/`). Missing `.en.md` falls back to Chinese.
- Switch: Material language selector + a `中文/EN` pill at the top-right (`docs/javascripts/header-links.js`); both jump to the same article in the other language.
- `hooks/autonav.py` also generates `index.en.md` (home + each category). English titles come from the `.en.md` frontmatter `title`.
- English reports live next to the Chinese ones in `/workspace/News/<cat>/` as `<same name>.en.md`; `sync.sh` mirrors both.
