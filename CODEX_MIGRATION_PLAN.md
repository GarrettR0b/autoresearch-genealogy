# Codex Migration Plan

Concrete checklist for moving `autoresearch-genealogy` from legacy tool-specific documentation to Codex-first documentation.

## Goal

Make Codex the default execution environment without changing the genealogy methodology, vault structure, or source rigor.

## Mandatory Outcomes

1. Codex is the default tool named in onboarding documentation.
2. Prompt execution instructions do not depend on any tool-specific slash command.
3. All prompts and related docs explicitly forbid invented facts.
4. All prompts and related docs explicitly require conflict reporting when sources disagree.
5. OCR and multimodal guidance use vendor-neutral terminology unless a vendor-specific note is intentional.
6. Agent instructions live in `AGENTS.md`, not only in `CLAUDE.md`.

## File by File Work

### 1. Root documentation

- `README.md`
  - Reposition the repo as Codex-first.
  - Replace legacy tool-specific quick start steps with Codex steps.
  - Link to `AGENTS.md` and this migration plan.

- `AGENTS.md`
  - Add repository-wide agent instructions for Codex.
  - Make evidence discipline mandatory.

- `CLAUDE.md`
  - Either deprecate it or trim it to a compatibility note after `AGENTS.md` is adopted.

### 2. Prompt system

- `prompts/README.md`
  - Replace legacy tool-specific execution instructions with Codex-oriented instructions.
  - Add a mandatory Evidence Discipline section.

- `prompts/*.md`
  - Add mandatory Guard bullets that forbid invention and require explicit conflict reporting.
  - Keep the 7-field prompt contract unchanged.

### 3. User workflows

- `workflows/getting-started.md`
  - Make Codex the default entry point.
  - Add a standard execution note that tells the agent not to invent facts and to surface conflicts.

- `workflows/ocr-pipeline.md`
- `workflows/document-triage.md`
  - Replace vendor-locked phrasing with vendor-neutral multimodal wording.
  - Keep tool examples practical.

### 4. Templates and references

- `vault-template/_Index.md`
- `vault-template/templates/transcription.md`
- `vault-template/templates/postcard.md`
- `vault-template/templates/certificate.md`
- `reference/what-ai-can-and-cannot-do.md`
  - Remove unnecessary vendor lock-in wording.
  - Preserve the research rigor and caution language.

## Required Prompt Guard Addition

Every prompt should contain guard language equivalent to this:

- Do not invent facts. Write only what is explicitly supported by the source text or by a clearly labeled inference.
- If sources conflict, do not merge them into one narrative. Record each version, cite each source, and mark the issue as unresolved until reconciled.
- If evidence is missing, say that it is missing.

## Suggested Rollout

1. Update root docs and `AGENTS.md`.
2. Update `prompts/README.md`.
3. Update all prompt files.
4. Update workflows.
5. Update templates and reference docs.
6. Add Codex-specific worked examples if needed.
