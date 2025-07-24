# Go Task Manager

A simple CLI task manager built in Go that helps you organize your daily tasks. It allows you to add, complete, list, and delete tasks directly from the terminal. All tasks are persisted locally using BoltDB.

## Installation

```bash
git clone https://github.com/bkandh30/goTaskManager.git
cd task-cli
go install .
```

## Usage

### Basic Usage

```bash
goTaskManager [command] [arguments]
```

### Commands

| Command  | Description             | Example                      |
| -------- | ----------------------- | ---------------------------- |
| `add`    | Add a new task.         | `./task add "Buy groceries"` |
| `list`   | List all tasks.         | `./task list`                |
| `do`     | Mark task as completed. | `./task do 1`                |
| `delete` | Delete a task.          | `./task delete 1`            |

### Examples

```bash
# Add a new task
goTaskManager add "Complete the project documentation"

# List all tasks
goTaskManager list

# Mark task with ID 1 as completed
goTaskManager do 1

# Delete task with ID 2
goTaskManager delete 2

# Add a task with spaces (use quotes)
goTaskManager add "Call mom and dad"
```

## Database

This CLI tool uses BoltDB, a pure Go key/value store, to persist tasks locally. The database file `tasks.db` will be created automatically in the same directory as the executable.
