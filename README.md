# Health Self-Investigation Skill

A Codex and Claude Code skill for investigating ambiguous, non-emergency health symptoms through intake, tracking, testing, analysis, and careful experiment planning.

The skill is designed to reduce activation energy for people who want to act on vague health questions like "I've been feeling more tired lately" without jumping straight to premature conclusions or unsafe experiments.

## What It Does

- Guides a short, high-yield intake in small batches.
- Helps choose what to track and what tests or clinician conversations may be useful.
- Analyzes logs, labs, notes, app exports, or wearable data when available.
- Helps plan low-risk, measurable experiments only when baseline context is sufficient.
- Helps prepare concise clinician messages and practical next steps.

This skill is not medical advice and does not replace a clinician. It is intended for organizing information, generating hypotheses, and planning safer next actions.

## Install In Codex

Use `$skill-installer` with the GitHub directory URL:

```text
$skill-installer install https://github.com/YOUR-USER/health-self-investigation-skill/tree/main/skills/health-self-investigation
```

Then restart Codex so the skill is loaded.

## Install In Claude Code

Copy the Claude Code skill folder into your Claude skills directory:

```bash
mkdir -p ~/.claude/skills
cp -R claude-skills/health-self-investigation ~/.claude/skills/
```

Then restart Claude Code. Invoke it with:

```text
/health-self-investigation I have been feeling more tired lately.
```

## Use Without Codex Or Claude Code

Copy the contents of:

```text
skills/health-self-investigation/references/portable-core.md
```

Paste it into ChatGPT, Claude, or another assistant's project/system instructions.

## Example Prompts

```text
Use $health-self-investigation. I've been feeling more tired lately.
```

```text
Use $health-self-investigation. I have two weeks of symptom logs and want help finding patterns.
```

```text
Use $health-self-investigation. I want to know what experiments are safe to try for my recurring afternoon crashes.
```

## Repository Layout

```text
skills/
  health-self-investigation/
    SKILL.md
    LICENSE.txt
    agents/
      openai.yaml
    references/
      portable-core.md
claude-skills/
  health-self-investigation/
    SKILL.md
    LICENSE.txt
    references/
      portable-core.md
```

## License

The skill is released under the MIT License. See `skills/health-self-investigation/LICENSE.txt`.
