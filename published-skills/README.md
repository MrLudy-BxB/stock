# Published Skills

This optional directory is for completed, repo-local shareable skill packages.

Do not place workflow files, raw sources, temporary files, logs, private notes, or unfinished drafts here.

## Add A Published Skill

Only copy a skill here when the user explicitly wants a repo-local shareable copy.

Copy from:

```text
projects/<project-id>/skill/<skill-name>/
```

To:

```text
published-skills/skills/<skill-name>/
```

## Published Skill Structure

```text
published-skills/
└── skills/
    └── <skill-name>/
        ├── README.md
        ├── SKILL.md
        ├── metadata.json
        └── references/
```

## Install From Local Repository

After a skill is copied here, install it from the repository root with:

```sh
npx skills add ./published-skills --skill <skill-name>
```
