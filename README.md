# Video Prompt Blueprint

A reusable Codex skill for writing structured AI video prompts from a concept and reference images. Developed from a 15-second fashion concept where a chrome ceiling fan conceals four outfit changes.

## What it captures

Seven sections: output specification; identity and references; camera and composition; main visual mechanism; timed action; transition rules; continuity and quality.

The creative pattern is **opening action → trigger → timed reveals → clear final hold**. Adapt it to fashion, product, or character videos without requiring a fan, overhead camera, five outfits, or a 15-second duration.

Includes explicit stationary-camera wording, designated reveal passes, and checks for timing, reference order, physical support, and concealment coverage. Prompt wording does not guarantee exact video-model behavior or viral performance.

## Use in Codex

Place this folder at `~/.codex/skills/video-prompt-blueprint` (or under your configured Codex skills directory). Start a new chat if necessary for skill discovery, then ask:

```text
Use $video-prompt-blueprint to write a 15-second fashion video prompt using five reference outfits, a stationary overhead camera, and a physical reveal transition.
```

For revisions:

```text
Use $video-prompt-blueprint to fix unwanted camera movement in this prompt while preserving my actions, reference order, and transition mechanism.
```

## Files

- [SKILL.md](SKILL.md): reusable instructions.
- [Prompt template](references/prompt-template.md): seven-section scaffold.
- [Original fan example](references/chrome-fan-example.md): original prompt plus adaptation notes.
- [Codex interface metadata](agents/openai.yaml): skill name and invocation example.

The reference example is an untested creative prompt. Uploaded reference photos and private account details are not included.
