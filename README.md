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

In Codex, paste this into the chat:

```text
$skill-installer install https://github.com/amydeng2000/health-self-investigation-skill/tree/main/skills/health-self-investigation
```

The `$` is part of the Codex skill invocation.

Then restart Codex so the skill is loaded.

## Install In Claude Code

### Option A: Claude Code Plugin Marketplace

This does not require cloning the repo.

From a terminal:

```bash
claude plugin marketplace add amydeng2000/health-self-investigation-skill
claude plugin install health-self-investigation@health-self-investigation
```

Or from inside Claude Code:

```text
/plugin marketplace add amydeng2000/health-self-investigation-skill
/plugin install health-self-investigation@health-self-investigation
```

Then restart Claude Code or run `/reload-plugins`. Invoke it with:

```text
/health-self-investigation:health-self-investigation I have been feeling more tired lately.
```

### Option B: GitHub CLI Agent Skill Installer

If your GitHub CLI supports `gh skill` (`gh >= 2.90.0`):

```bash
gh skill install amydeng2000/health-self-investigation-skill health-self-investigation --agent claude-code --scope user
```

If `gh` says `unknown command "skill"`, update GitHub CLI or use Option A.

### Option C: Manual Fallback

If you prefer a plain, non-plugin Claude Code skill, clone or download the repo and copy the Claude Code skill folder into your Claude skills directory:

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

### Codex

```text
Use $health-self-investigation. I've been feeling more tired lately.
```
### Claude Code Plugin Install

If installed through the Claude Code plugin marketplace, use the plugin-qualified slash command:

```text
/health-self-investigation:health-self-investigation I've been feeling more tired lately.
```

### Claude Code Manual Skill Install

If copied manually into `~/.claude/skills`, use the skill slash command:

```text
/health-self-investigation I've been feeling more tired lately.
```

```text
/health-self-investigation I have two weeks of symptom logs and want help finding patterns.
```

```text
/health-self-investigation I want to know what experiments are safe to try for my recurring afternoon crashes.
```

### ChatGPT, Claude, Or Other Chat Interfaces

After pasting `portable-core.md` into project/system instructions, ask naturally:

```text
I've been feeling more tired lately. Please use the health self-investigation process.
```

## License

The skill is released under the MIT License. See `skills/health-self-investigation/LICENSE.txt`.
