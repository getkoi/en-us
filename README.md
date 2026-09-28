# EN-US

EN-US writes and revises concise, natural US English. It leads with the main point, simplifies technical language, and removes filler while preserving meaning and voice.

## Install as a skill

Install from a local copy with [skills.sh](https://skills.sh/):

```bash
npx skills add /path/to/en-us --skill en-us
```

Replace `/path/to/en-us` with this package's directory. The command installs the skill for your current project. Add `--global` to make it available across projects.

## Use

Invoke the skill explicitly:

- `/en-us` in compatible agents
- `$en-us` in Codex

```text
/en-us Rewrite this text in concise US English. Keep the facts and my voice.
```

```text
$en-us Explain how this retry policy works for a reader who is new to APIs.
```

For voice matching, provide a writing sample. For file editing, name the file and the prose to revise. Ask for an explanation of the changes if you want one; the default response is the finished text alone.

## Writing defaults

- Put the answer first. Cut repeated context, empty framing, and generic closings.
- Prefer familiar words, concrete verbs, and consistent terms. Review sentences over 25 words.
- Preserve facts, conditions, uncertainty, requirement strength, and necessary detail.
- Use American spelling and consistent editorial conventions. Keep natural contractions and the author's voice.
- Use bullets, numbered lists, or a small diagram when they make the explanation easier to follow.

Sentence lengths are flexible targets. A longer explanation is welcome when it prevents a misunderstanding. The skill preserves code, commands, paths, identifiers, frontmatter, data, and link destinations during prose edits.

## Example

Before:
> In order to continue with the setup process, it is necessary for you to verify your email address using the link that we sent you.

After:
> To continue setup, verify your email with the link we sent you.

More examples cover technical conditions, voice matching, US localization, and Markdown files in [examples.md](skills/en-us/references/examples.md).

## Plugin for ChatGPT and Codex

The root `plugin.json` is the portable Agent Plugins manifest. `.codex-plugin/plugin.json` provides compatibility with clients that use the Codex-specific format.

The package contains one skill. It runs without an MCP server, authentication, or external service. Plugin installation and discovery depend on the client's supported package workflow.

## Plugin for Claude Code

Load the local plugin:

```bash
claude --plugin-dir /path/to/en-us
```

Then invoke its qualified skill name:

```text
/en-us:en-us Rewrite this text in concise US English.
```

For a persistent local marketplace installation, run these commands inside Claude Code:

```text
/plugin marketplace add /path/to/en-us
/plugin install en-us@en-us
```

## Structure

- [`skills/en-us/SKILL.md`](skills/en-us/SKILL.md): core instructions and final review checklist.
- [`skills/en-us/agents/openai.yaml`](skills/en-us/agents/openai.yaml): presentation and explicit-invocation policy.
- [`plain-english.md`](skills/en-us/references/plain-english.md): technical clarity, conditions, procedures, and diagrams.
- [`us-style.md`](skills/en-us/references/us-style.md): US conventions and house choices.
- [`patterns.md`](skills/en-us/references/patterns.md): editing patterns with original examples.
- [`examples.md`](skills/en-us/references/examples.md): worked rewrites and preservation checks.
- [`plugin.json`](plugin.json), [`.codex-plugin/plugin.json`](.codex-plugin/plugin.json), [`.claude-plugin/plugin.json`](.claude-plugin/plugin.json), and [`.claude-plugin/marketplace.json`](.claude-plugin/marketplace.json): plugin packaging.

## Sources and editorial choices

- [ASD-STE100](https://www.asd-ste100.org/) and its [Wikipedia overview](https://en.wikipedia.org/wiki/Simplified_Technical_English): clear sentences, consistent terminology, and explicit instructions.
- [The Chicago Manual of Style](https://www.chicagomanualofstyle.org/home.html): selected US-English editorial conventions.
- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing): patterns of formulaic prose.

EN-US is a practical house style. It uses STE-inspired principles without reproducing the official dictionary or certifying compliance. Sentence-case headings, small-number styling, flexible length targets, and final-only output are its own choices. References distinguish those choices from the source conventions.

## License

[MIT](LICENSE). External standards and linked resources retain their own licenses.
