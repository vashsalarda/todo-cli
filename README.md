// ...existing code...
# Todo CLI

A simple command-line todo application written in Go. It stores todos in `todos.json` and provides basic operations via command-line flags.

## Files
- `main.go`
- `command.go` 
- `storage.go`
- `todo.go`
- `todos.json`

## Prerequisites
- Go 1.18+

## Build
```powershell
go build -o todo-cli .
```

## Usage examples
- List todos:
```powershell
.\todo-cli -list
```
- Add a todo:
```powershell
.\todo-cli -add "Buy milk"
```
- Edit a todo (format: index:new_title):
```powershell
.\todo-cli -edit "0:Buy almond milk"
```
- Toggle completion:
```powershell
.\todo-cli -toggle 0
```
- Delete a todo:
```powershell
.\todo-cli -del 0
```

## Notes
- Todos are loaded from and saved to `todos.json` via `NewStorage` in `storage.go`.
- See `command.go` for available flags and usage details.