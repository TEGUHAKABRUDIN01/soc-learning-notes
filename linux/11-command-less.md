# Linux Command - less

## Objective

Learn how to read large files interactively without loading the entire file at once.

## Syntax

```bash
less [options] file_name
```

## Common Options

- `-N` → Show line numbers.
- `-F` → Exit automatically if the file fits on one screen.

## Useful Keys

- `Space` → Next page
- `b` → Previous page
- `g` → First line
- `G` → Last line
- `/pattern` → Search text
- `n` → Next match
- `N` → Previous match
- `q` → Quit

## SOC Use Cases

- Read `/var/log/auth.log`
- Read `/var/log/syslog`
- Search authentication events
- Navigate large log files efficiently

## Learning

`less` is preferred over `cat` for reading large log files because it allows interactive navigation and searching without displaying the entire file at once.