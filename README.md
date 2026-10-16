# Godot AI Agent Rules (Free Mini)
Three Cursor rules and an AGENTS.md that stop the most common AI mistakes in Godot 4: Godot 3 syntax (`yield`, `export`, `onready`, `KinematicBody2D`, `instance()`, old `connect()`), made-up APIs, and missing parse checks.

**Install:** copy `.cursor/` and `AGENTS.md` into your Godot project root, next to `project.godot`. For ChatGPT or Claude chat, paste `PRIMING_HEADER.md` at the start of the conversation.

**Check your scripts:** `godot --headless --check-only --script res://player.gd` parses a script without opening the editor.

**Want more?** The full **Godot AI Agent Kit** adds typed GDScript, signals/Callables, node paths & %unique names, resources/saving, C# and test rules, a CLAUDE.md, a phased planning workflow with templates, 20 task prompts (controllers, FSM, save/load, inventory, dialogue, UI...), a whole-project headless check script, and tested samples. [Get it on itch.io](ITCH_URL_TBD)

License: MIT. Not affiliated with the Godot Foundation.
