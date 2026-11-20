# Surface Content

**Bring more of your website's content to the surface.**

Help your coding agent make your website's content easier to find, edit and maintain—without changing what makes your website unique.

Free and open source. Works with or without Surface CMS.

> **Early candidate:** This repository is being prepared for its first release. Installation instructions describe documented agent capabilities; the skill has not yet been qualified in representative agent and website workflows. Review the exact revision before trying it on a disposable branch. No stable release is announced yet.

## What it does

Surface Content is a portable [Agent Skill](https://agentskills.io/specification) for custom websites. It helps a coding agent recognize content hidden in application code, choose a sensible editorial home, and preserve the site's design, behavior, ownership and ability to adopt future framework releases.

It can review a whole website, make a cohesive set of worthwhile improvements, help with a particular page, or guide normal page development. It may recommend leaving well-organized content alone. It does not prescribe a CMS, markup syntax, folder structure or framework. Astro and Next.js examples illustrate the principles; other frameworks are welcome. Actual operation in a particular agent or framework is not guaranteed.

If an applicable Surface CMS contract already exists, the agent can maintain its relevant mappings in the same authorized contribution. A contract-only correction can be sufficient. If there is no contract, the skill works normally and adds none. No Surface login, API or hosted service is needed. The skill does not make every file or region writable in Surface; the product's own eligibility and Save checks still govern.

## Get the skill

The package is [`skills/surface-content/`](skills/surface-content/), including `SKILL.md`, both references, and the license. Inspect the contents at a reviewed commit or release. Copy or install the **whole directory**, not just the main instruction file.

### Manual installation

Download the source of the reviewed revision through GitHub and copy the package into the skill directory documented for your agent. Keep its directory name and relative paths. Common documented project locations (the full resulting path ends in `surface-content/SKILL.md`):

| Agent/mode | Parent directory | Guidance |
| --- | --- | --- |
| GitHub Copilot cloud coding agent | `.github/skills/`, `.claude/skills/` or `.agents/skills/` | [Copilot skills](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills) |
| Claude Code local | `.claude/skills/` | [Claude Code skills](https://code.claude.com/docs/en/skills) |
| Codex local | `.agents/skills/` | [Codex skills](https://learn.chatgpt.com/docs/build-skills) |
| Cursor local | `.cursor/skills/` or `.agents/skills/` | [Cursor skills](https://cursor.com/docs/skills) |

For personal installation, use your agent's documented user-level location. Local personal copies are not necessarily available in cloud tasks. A cloud agent needs the skill in its accessible project revision or another supported, explicitly authorized scope. Check that the agent discovers the correct skill, start a fresh session if needed, and name it in your request. Avoid conflicting copies. Commit a project installation only if your repository's owners authorize ongoing agent guidance.

### GitHub CLI (optional)

The [`gh skill install` command](https://cli.github.com/manual/gh_skill_install) is in public preview. If your installed CLI supports it, inspect the selected revision and both references first. Set `REVIEWED_SHA` to the full commit SHA you inspected (do not run with an empty value). For example, at the root of the website repository:

```sh
gh --version
gh skill install orwarhol/surface-content surface-content --agent github-copilot --scope project --pin "$REVIEWED_SHA"
```

For a personal Claude Code installation, choose `--agent claude-code --scope user`. For local Codex or Cursor, select `codex` or `cursor` as the agent. Inspect the installed location and all package files. These are documented installer options, not a claim that this candidate has been tested with those hosts. If the command is unavailable, use the manual method.

For one-time use, a host with suitable tools may be able to read the complete skill and needed references from the same reviewed revision without installing it. This is optional; a repository link alone does not prove that the agent read the files. Use a local reviewed copy if retrieval is blocked or incomplete. Do not grant new network or repository privileges just to run the skill.

## Suggested prompts

Use these once the skill is available to your agent. In a monorepo, name the intended website if it is not obvious.

### Review my website

> Use the Surface Content skill to review my website for opportunities to make its content easier to find, edit and maintain. Recommend worthwhile improvements without making changes.

### Improve my website

> Use the Surface Content skill to make more of my website's content independently editable. Preserve its design, functionality and framework conventions. If an existing Surface CMS contract is present, update it where appropriate. Submit your improvements in one Pull Request.

### Improve a particular page

> Use the Surface Content skill to make the content on my homepage easier to edit and maintain while preserving its existing design and functionality.

### Build with maintainable content

> Apply the Surface Content skill while building or modifying pages on my website. Organize editorial content so that it remains easy to find and maintain independently of the application code.

The agent should explain what became easier to edit, where the content now lives, what it intentionally preserved, any applicable contract changes, and what it actually checked. Review the diff before merging; installation or invocation never grants permission to merge or publish.

## Updating and contributing

Review a new release and its exact revision before replacing an installed copy. Preserve local modifications and use normal repository review for project updates. Do not force an update or remove a pin merely to get the newest version.

Questions, examples and ordinary feedback are welcome in GitHub issues. Use synthetic examples; do not include customer code, tokens, configuration secrets or other private material. Submit only contributions you have the right to license under MIT and identify any third-party material and its license. See [security reporting](SECURITY.md) for sensitive issues.

[MIT license](LICENSE). Surface Content is instructions and examples, not a hosted integration. It adds no telemetry or Surface data recipient; your coding agent and its environment govern access and processing.
