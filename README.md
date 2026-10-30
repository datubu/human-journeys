# Human Journeys · 人类远行档案

The single content source for Datubu. 一个内容源，九个网站。

Routes, chapters, people, places and source references are plain Markdown with YAML frontmatter. Geography is stored separately as GeoJSON. Chinese and English records use `.zh.md` and `.en.md`, sharing the same stable ID.

## First complete example / 首个完整案例

- [玄奘西行](routes/xuanzang/index.zh.md)
- [Xuanzang’s Journey](routes/xuanzang/index.en.md)
- 11 paired chapters, 10 paired place records, one paired person record, seven paired source records.
- Map lines are regional schematics, not surveyed trails or modern navigation.

## Edit and build / 编辑与构建

1. Edit Markdown here, preserving entity IDs and both languages.
2. Run `node ../journeys/scripts/build-all.mjs` from this sibling-repository workspace.
3. Run `node ../journeys/scripts/verify.mjs` to verify content references and all site outputs.

Only `status: published` routes appear in the built sites. Introduction-only stations do not invent route content. Source records link to external publications; images or text at those links are not automatically licensed for reuse.

## Publication

Publication is intentionally deferred. No GitHub remote, Pages setting or DNS record is configured by the local scaffold. Owner-specific workflow variables are configured at upload time; see the `journeys` deployment guide.

## Contributions and rights

Original prose and schematic geography use CC BY 4.0; see LICENSE.md. Software is licensed separately under MIT. Newly authored prose in this scaffold is original; third-party source material is referenced, not bundled. Code, prose, geography and third-party assets must keep separate rights records.
