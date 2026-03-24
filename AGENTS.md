# AGENTS.md

Instructions for Codex and other repository-aware agents working in `autoresearch-genealogy`.

## Repository Purpose

This repository is a prompt pack and knowledge base for AI-assisted genealogy research. The main assets are the prompt files, vault templates, workflows, archive guides, and reference material.

## Read This First

When starting work in this repository, read these files in order:

1. `README.md`
2. `prompts/README.md`
3. `workflows/getting-started.md`
4. `CODEX_MIGRATION_PLAN.md` if the task is about Codex migration

## Prompt Contract

Every prompt in `prompts/` is expected to preserve these fields:

- Goal
- Metric
- Direction
- Verify
- Guard
- Iterations
- Protocol

Do not remove any of these fields when editing prompts.

## Evidence Discipline, Mandatory

These rules are mandatory for all prompts, workflows, examples, and vault templates:

- Do not invent facts, names, dates, places, relationships, document contents, or sources.
- Write only what is supported by the source text, or by a clearly labeled inference that is explicitly marked as an inference.
- If sources conflict, do not merge them into one story. Record each version separately, cite each source, and mark the issue as unresolved or conflicting until it is reconciled.
- If the evidence is incomplete, say that the evidence is incomplete.
- Use concise, dry wording. Prefer extraction, tables, and comparison over dramatic narrative.
- Negative results are valuable. Log them.

## Vault Conventions

- All vault files use YAML frontmatter with at minimum: `type`, `created`, `tags`.
- Person files add: `name`, `born`, `died`, `family`, `confidence`, `sources`.
- Transcription files add: `source`, `document_type`, `person`, `date`, `ocr_method`, `ocr_quality`.
- Wikilinks use underscores in filenames, not spaces.

## Style

- No hyphens as punctuation. Use commas, periods, colons, semicolons, or parentheses.
- No emojis in repository content.
- Source-first. Unsourced claims should be flagged.
- Use confidence tiers consistently.
