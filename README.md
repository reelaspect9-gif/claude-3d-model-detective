# 3D Model Detective for Claude Code

A standard Claude Code subagent that **diagnoses, repairs, and verifies** unwanted model intersections, clipping, z-fighting, exposed corners, and related integration defects. It performs targeted reversible fixes within its assignment and returns corrected artifacts with evidence.

Repository: [reelaspect9-gif/claude-3d-model-detective](https://github.com/reelaspect9-gif/claude-3d-model-detective)

Agent definition: [3d-model-detective.md](.claude/agents/3d-model-detective.md)

Download: [raw agent Markdown](https://raw.githubusercontent.com/reelaspect9-gif/claude-3d-model-detective/main/.claude/agents/3d-model-detective.md)

## What it does

The agent reproduces a defect, distinguishes unintended penetration from intentional contact or overlap, finds the underlying cause, chooses an appropriate repair, and checks affected motion and dependent shots. For a square component protruding through a curved shell, it may correct placement or reshape/chamfer the offending region after examining the actual construction. It does not blindly delete faces or shrink every part.

The instructions preserve dimensions, silhouette, material mapping, required texture detail, rigging, functional controls, typography, illustrated character rules, and accepted animation. They distinguish candidate collision tests from actual geometric evidence and require honest reporting of incomplete checks.

This is a repair worker, not an independent final reviewer. Production Quality Director retains that review role. The existing Prompt Engineer, supporting Prompt Architect, and Font Expert remain part of the team.

## Install in the intended scope

Read the complete definition before adopting it. Save the raw Markdown at one standard Claude Code location:

- Project: `<your-project>/.claude/agents/3d-model-detective.md`
- User: `~/.claude/agents/3d-model-detective.md`

Create missing directories as appropriate. On Windows, user scope normally resolves under `%USERPROFILE%\.claude\agents\`. Use the actual Claude project or user configuration directory; avoid an accidental nested repository folder or conflicting copies in both scopes.

Inspect any existing same-name file first. Preserve its customizations and compare the definitions. Prepare amendments separately and obtain explicit replacement permission before erasing existing content. Installing a missing file within authorized setup does not require a redundant approval.

Keep the UTF-8 Markdown contents, YAML frontmatter, and exact `.md` extension. Do not save a GitHub HTML preview as the agent definition. The file uses `name` and `description` frontmatter and does not hardcode a model, tool list, hooks, credentials, or permission bypass.

See the [official Claude Code subagent documentation](https://code.claude.com/docs/en/sub-agents) for the current supported format and discovery behavior. If the definition is not discovered, inspect its location and frontmatter and start a fresh Claude Code session as needed. Do not assume `/3d-model-detective` is a slash command.

## Delegate a concrete repair

Example request to the lead:

> Use the 3d-model-detective subagent to diagnose and repair the square component that protrudes through this curved shell. Provide the actual scene, active blueprint and style rules, affected object names, failing frames, camera, and assigned source files. Preserve a recoverable baseline. Correct the root cause within scope, inspect the full relevant motion and dependent shots, and return changed artifacts plus before/after evidence. Then send the repair to Production Quality Director for independent review.

For a broader task, provide an asset or shot inventory and clear ownership boundaries. Define which contact relationships are intended and which are defects. The lead must actually delegate the work and supply usable files and tools; the agent does not automatically monitor every operation.

## Verify the first invocation

Use a small representative repair on a recoverable working copy. Confirm runtime discovery, actual delegation, saved changes, and appropriate geometry/render checks separately. Ask the agent to distinguish verified fixes from untested changes and unresolved inputs. A listed agent or successful script exit is not proof that the final asset looks correct.

## Capabilities and status

This repository does not install Blender, a modeling API, rendering software, or other agents. Execution depends on the tools available in the actual Claude environment. The definition has **not been live-tested in Claude Code**. It is not a background daemon, automatic interceptor, permission system, or guarantee of perfect models.
