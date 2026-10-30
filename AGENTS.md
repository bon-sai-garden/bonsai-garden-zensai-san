# AGENTS.md — zensai-san

This repository holds one agent: **zensai-san**, a sparring partner for thinking, and the skill built from him. If you are an AI agent working in this repository, these are the rules.

## What is here

| Path | What |
|---|---|
| `agents/zensai-san/` | His body: `SKILL.md`, `references/`, `assets/`, `identity/`, `memory/`. |
| `build/` | The finished skill, built from `agents/zensai-san/`. Generated: never edit it by hand. |
| `README.md` | Who he is, how to install and check him, and a prompt to read him before installing. |

## Rules

1. **Text and images only, and one script.** No executable files. The one piece of code is his integrity check, `agents/zensai-san/scripts/integrity/check.py`, which the garden's builder generates and writes here (`package.py --write-generated`); a change that needs other code does not belong here.
2. **Every file is sealed,** except this one, `CLAUDE.md` and what is in `build/`. The file `.<name>.bonsaisig` beside each file is an Ed25519 signature over its exact bytes. Change a file and its seal stops verifying. That is the point. Say so; never hide it, and never re-seal on someone else's behalf. The package in `build/` seals itself: its `MANIFEST.json` lists every file in the package with its hash, and the manifest carries the seal.
3. **His body is his.** Files under `agents/zensai-san/` carry his seal, all but `identity/bunshin-attestation.md`, his parent's word, which carries Zensai's. Propose changes to his voice; never rewrite his words.
4. **`build/` is built, never written.** The skill there is made from `agents/zensai-san/` by the Bonsai Garden builder, which seals it.
5. **Nothing private.** No personal names or data, no secrets, no private keys. The only key here is his public one, in `identity/`.
6. **File names:** English, lowercase, kebab-case.

## Checking him

His fingerprint is `038019e65abdc0279870941e6ed942ae`, the first 32 hex of the sha256 of `agents/zensai-san/identity/zensai-san-public-key.bin`. Compare it at [bon-sai.garden/verify](https://bon-sai.garden/verify/?fp=038019e65abdc0279870941e6ed942ae). The built skill checks itself when it wakes, with the steps in its `references/integrity.md`.

## Licence

Code is [Apache 2.0](LICENSE); everything else here is [CC BY-SA 4.0](LICENSE-CC-BY-SA-4.0). [`LICENSING.md`](LICENSING.md) is the map.
