# Godot AI Agent Rules (Free Mini)
Three Cursor rules and an AGENTS.md that stop the most common AI mistakes in Godot 4: Godot 3 syntax (`yield`, `export`, `onready`, `KinematicBody2D`, `instance()`, old `connect()`), made-up APIs, and missing parse checks.

### Also catches runtime errors that pass `--check-only`
| AI writes | Godot 4 says | Fix |
|---|---|---|
| `add_child(coin)` inside `body_entered` | "Can't change this state while flushing queries" | `add_child.call_deferred(coin)` (full kit) |
| `.bind("weapon")` with handler `(slot, index)` | "Cannot convert argument 1 from int to String" | Bound args come last: `(index, slot)` (full kit) |
| `$HUD/MarginContainer/HealthBar` | "Node not found", then "null instance" | `%HealthBar` or an `@export` reference (full kit) |

## Quick start
1. `git clone https://github.com/scoyoc5/godot-ai-agent-rules`
2. Copy `.cursor/` and `AGENTS.md` next to your `project.godot`.
3. Ask your agent: *"Make the player jump."* It should use `await`, `@export` and `CharacterBody2D`, never Godot 3 syntax.
4. Verify: `godot --headless --check-only --script res://player.gd`

**Install:** copy `.cursor/` and `AGENTS.md` into your Godot project root, next to `project.godot`. For ChatGPT or Claude chat, paste `PRIMING_HEADER.md` at the start of the conversation.

**Check your scripts:** `godot --headless --check-only --script res://player.gd` parses a script without opening the editor.

**Want more? 🎃 25% off in the itch.io Halloween Sale (Oct 25 – Nov 4).** The full **Godot AI Agent Kit** adds typed GDScript, signals/Callables, node paths & %unique names, resources/saving, C# and test rules, a CLAUDE.md, a phased planning workflow with templates, 20 task prompts (controllers, FSM, save/load, inventory, dialogue, UI...), a whole-project headless check script, and tested samples. [Get it on itch.io](https://johnvanscoyoc.itch.io/godot-ai-agent-kit-rules-prompts-workflow-for-cursor-and-claude-code)

License: MIT. Not affiliated with the Godot Foundation.

<sub>Keywords: cursor rules for godot, .cursorrules godot, claude code godot 4, CLAUDE.md gdscript, AGENTS.md godot, chatgpt godot 4, yield to await, KinematicBody2D to CharacterBody2D.</sub>
