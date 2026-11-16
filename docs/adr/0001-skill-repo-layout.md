# Skill repo layout: root docs + `skills/<name>/SKILL.md` + topic modules

Skills ship as `skills/<name>/SKILL.md` (registry frontmatter + Markdown) so each skill is self-contained and portable to any agent harness; per-skill bundled data (the myth catalog) lives in `topics/<topic>/` inside the skill that reads it, so adding a topic is copying a skeleton; cited research stays under `research/`, separate from shipped skill content. The end-user skill answers in chat only, so there is no `rebuttals/` output directory.
