# todo-slash-command
A .claude slash command to manage a simple todo list in your project's root directory, without having to leave Claude Code!

## Inspiration
You ever been in the midst of a vibe-session and thought, "Oh, I need to fix the padding on that button". Well, no need to even leave the claude interface. Just use this `/todo` slash-command to create and manage a simple todo list for your project, from **within** your project.

Once the `todos.md` file is created in your project's root directory, you can probably even just tell claude to add to it without having to use the slash-command, but the slash-command provides some nifty commands for your benefit.

## Install
Download [todos.md](todos.md) or copy its contents and place it in 1 of 2 locations...

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

## Available Commands
All commands begin with `/todo`, followed by any of the following available commands:
 - `add "task description"` - Add a new todo
 - `add "task description" [tomorrow|next week|4 days|June 9|12-24-2025|etc...]` - Add a new todo with the provided due date
 - `due N [tomorrow|next week|4 days|June 9|12-24-2025|etc...]` - Mark todo N with the due date provided
 - `complete N` - Mark todo N as completed and move from the ##Active list to the ##Completed list
 - `remove N` - Remove todo N entirely
 - `undo N` - Mark completed todo N as incomplete
 - `list [N]` or no args - Show all (or N number of) todos in a user-friendly format, with each todo numbered for reference
 - `past due` - Show all of the tasks which are past due and still active
 - `next` - Shows the next active task in the list, this should respect Due dates, if there are any. If not, just show the first todo in the Active list


## Usage Examples:
- `/todo add "Fix navigation bug"`
- `/todo add "Fix navigation bug" [date/time/"tomorrow"/"next week"]`
  - **Optional:** due date can be provided
- `/todo complete 1` 
- `/todo remove 2`
- `/todo list`
- `/todo undo 1`

Any questions? Feel free to reach out and send me a message!
