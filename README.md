# PPTPRO

PPTPRO is a Codex skill for building polished, editable PPT/PPTX decks with a strict production workflow.

It focuses on:

- a mandatory anti-AI design gate for composition, typography, color, copy, imagery, and decoration
- a six-pass design workflow: distill, layout, typeset, colorize, calibrate, and polish
- an optional Zinx liquid-glass pixel-particle presentation direction with semantic red/yellow/blue/green roles
- slide recipe planning instead of generic bullet decks
- visual enrichment for text-heavy presentations
- source-native figures and real source objects for evidence-backed decks
- generated content visuals with the current latest built-in Codex/ChatGPT image tool when no real or traceable image fits
- softer rounded cards, callouts, panels, and synthesis bars
- human-facing source text instead of internal workflow notes
- rendered preview inspection and strict PPTX audit before handoff

## Files

- `SKILL.md`: main skill behavior and workflow
- `references/design-system.md`: PPTPRO visual language and QA rules
- `references/slide-recipes.md`: reusable slide structures
- `references/anti-ai-design.md`: anti-AI design gate and rendered-review criteria
- `references/zinx-style.md`: optional Zinx presentation art direction
- `scripts/pptpro_audit.py`: strict PPTX audit helper
- `agents/openai.yaml`: agent metadata and default prompt

## Audit

Run the audit helper on a local deck:

```bash
python scripts/pptpro_audit.py path/to/deck.pptx --render --strict
```

For decks with speaker scripts:

```bash
python scripts/pptpro_audit.py path/to/deck.pptx --script path/to/script.docx --render --strict
```

The audit checks common PPTPRO defects such as text overflow, cramped cards, missing shell slides, forbidden serif/beige defaults, internal workflow text inside audience-facing content, and weak visual balance.
