# todo-slash-command
A .claude slash command to manage a simple todo list in your project's root directory, without having to leave Claude Code! Todos are stored in `todos.md` at your project root and automatically numbered for easy reference.

## Inspiration
You ever been in the midst of a vibe-session and thought, "Oh, I need to fix the padding on that button". Well, no need to even leave the claude interface. Just use this `/todo` slash-command to create and manage a simple todo list for your project, from **within** your project.

Once the `todos.md` file is created in your project's root directory, you can probably even just tell claude to add to it without having to use the slash-command, but the slash-command provides some nifty commands for your benefit.

## Install
Download [todo.md](todo.md) or copy its contents and place it in 1 of 2 locations...

### 1. Personal command (✨ recommended)
...your home directory: `~/.claude/commands/todos.md`.

**Note:** This will make the command available across **all** your projects.

### 2. Project command
...your project's root directory: `[your project's root directory]/.claude/commands/todos.md`.

**Note:** This will store the command in your repository and allow it to be shared with your team

## Features
- As a global slash command, knows to create todos in your current project's root directory
- Can set due dates (`/todo 1 due tomorrow` or `/todo 3 due 5pm` etc.)
- Lists todo tasks sorted by due date, if specified (`/todo list`)
- Knows your next todo item (`/todo next`)
- Add, complete, undo todo items

## Available Commands & Usage Examples

### Add todos:
  - `/todo add "Fix navigation bug"`
  - `/todo add "Fix navigation bug" tomorrow`
  - `/todo add "Fix navigation bug" "June 25"`

### Manage todos:
  - `/todo complete 1` - Mark todo #1 as completed
  - `/todo remove 2` - Delete todo #2 entirely
  - `/todo undo 1` - Move completed todo back to active
  - `/todo due 1 tomorrow` - Add due date to todo #1

### View todos:
  - `/todo list` - Show all todos (numbered)
  - `/todo list 5` - Show first 5 todos
  - `/todo next` - Show next task (respects due dates)
  - `/todo past due` - Show overdue tasks

### Date Formats:
All of the following formats are acceptable for specifying due dates:
  - "tomorrow", "next week", "4 days"
  - "June 25", "12-24-2025"
  - Times: "tomorrow 3pm", "June 25 2:30 PM"

## Questions?
Any questions? Feel free to reach out and send me a message!
