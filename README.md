# Agent Skills

Reusable skills I built for coordinating engineering work, reviewing security, designing interfaces, and checking claims. These packages were moved from [ML-AI-Projects](https://github.com/pablorod11/ML-AI-Projects) on October 31, 2026.

## Skills

| Skill | Purpose | Instructions |
| --- | --- | --- |
| [Napolean](napolean/README.md) | Coordinate bounded specialist missions and verify the integrated result. | [SKILL.md](napolean/SKILL.md) |
| [Napolean Security](napolean-security/README.md) | Coordinate scoped security reviews and validate findings against evidence. | [SKILL.md](napolean-security/SKILL.md) |
| [Design Workflow](design-workflow/README.md) | Coordinate interface direction, implementation, audits, and browser checks. | [SKILL.md](design-workflow/skills/design-workflow/SKILL.md) |
| Awesome Design References | Find concrete design references from the attributed bundled catalog. | [SKILL.md](design-workflow/skills/awesome-design-references/SKILL.md) |
| [Euclidean](euclidean/README.md) | Check claims against stated premises, with a standalone capacity checker. | [SKILL.md](euclidean/SKILL.md) |

## Install

Clone this repository and copy only the skill packages you want into your agent’s supported skills directory. For Codex’s default personal directory:

```sh
git clone https://github.com/pablorod11/agent-skills.git
cd agent-skills
mkdir -p ~/.codex/skills
cp -R napolean napolean-security euclidean ~/.codex/skills/
cp -R design-workflow/skills/design-workflow design-workflow/skills/awesome-design-references ~/.codex/skills/
```

Review existing installations before copying; these commands can overwrite files in folders with the same names. If `CODEX_HOME` is configured, use its `skills/` directory instead. See each package README for dependencies and usage.

Installing the coordinating instructions does not install their external tools, specialist skills, browsers, or optional runtimes. Those remain separate dependencies.

## Check the capacity example

Euclidean’s checker uses the Python standard library:

```sh
python3 euclidean/scripts/ecc.py --self-test
python3 euclidean/scripts/ecc.py euclidean/examples/capacity.json
```

Package READMEs retain their original dated validation notes and limits. Moving the files does not rerun or renew those broader validations.

## Provenance and attribution

`migration-manifest.json` records the original ML-AI-Projects commit and SHA-256 hashes before and after the move. The skill instructions and support files are preserved; installation paths in two package READMEs were updated for this repository. The source repository retains its earlier Git history.

Existing license and attribution notices are preserved, including the bundled Awesome Design catalog’s license. The collection does not add a blanket license over third-party material or claim affiliation with the upstream projects referenced by the skills.
