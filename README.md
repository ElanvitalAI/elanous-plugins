# Elanous plugins

The official, free Elanous plugin marketplace. Each plugin is a set of skills — and, for Elanous, graphs — signed and published with `elanous market publish`.

| Plugin | What it adds |
|---|---|
| `elanous-basics` | Web search and crawling (`omni-crawl`), link digests (`omni-digest`), project onboarding (`project-onboarding`), a grilling interviewer (`grill-me`), photo OCR intake (`photo-intake-ocr`) |
| `elanous-media` | Building videos (`video-builder`) and word-timed motion B-roll (`motion-broll`) |
| `video-broll` | Cut word-timed motion B-roll into a talking-head video — the first plugin with a graph (`graphs/broll-line.yaml`) |

## Install in Codex

```bash
codex plugin marketplace add ElanvitalAI/elanous-plugins
codex plugin add elanous-basics@elanous
```

## Verify

`marketplace.json` is signed as bytes by `index.sig` (Ed25519). The official public key is `keyId 4d809b69` — the same key Elanous trusts by default. Each package under `<plugin>/<version>/<sha256>.tgz` matches the `artifact.sha256` in the index.

- Signed index (static): https://elanvitalai.github.io/elanous-plugins/marketplace.json
- Build your own plugin: https://github.com/ElanvitalAI/elanous/blob/main/docs/build-a-plugin.md

## Licenses

Apache-2.0 (see `LICENSE`), except `skills/motion-broll/` inside `elanous-media` and `video-broll`, which is MIT from Barty-Bart/motion-graphics (its own `LICENSE` and `SOURCE.md` are included; the bundled Geist fonts are OFL).
