# bash2mac

Setup bash as default shell on macos.

## Install

Install the latest bash and GNU utilities, so that bash behaves as on linux:

```
curl -L https://raw.githubusercontent.com/docdnp/bash2mac/main/setup-bash | sh
```

In case you also want to set the bash as the default shell:

```
curl -L https://raw.githubusercontent.com/docdnp/bash2mac/main/setup-bash -o /tmp/setup-bash
chmod +x /tmp/setup-bash
/tmp/setup-bash --use-as-default-shell
```

## Shortcuts

Activate "Option as Meta" in your terminal (Shortcut: `Command + Option + O`).
This allows you to use the following shortcuts described below.
Most shortcut insertions are executed at the "current cursor position" (CCP).
Those that are always applied to the "end of line" (EOL) are marked with EOL.

### Shortcuts: Special characters

| Shortcut    | Character  |
| ----------- | ---------- |
| ⌥ + 1       | ~          |
| ⌥ + 5       | [          |
| ⌥ + 6       | [          |
| ⌥ + 7       | \|         |
| ⌥ + 8       | {          |
| ⌥ + 9       | }          |
| ⌥ + ß       | \\         |
| ⌥ + q       | @          |
| ⌥ + ⌃ + e   | €          |

### Shortcuts: History and line actions

| Shortcut    | Action                |
| ----------- | --------------------- |
| ⌥ + 2       | top of history        |
| ⌥ + 3       | end of history        |
| ↑           | prev. history item    |
| ↓           | next history item     |
| ⇧ + ←       | start of line         |
| ⇧ + →       | end of line           |
| ⌥ + ←       | move one word left    |
| ⌥ + →       | move one word right   |
| ⌥ + ⌫       | del previous word     |
| ⌥ + -       | del next word         |
| ⌫           | del previous char     |
| ⌥ + ö       | del next char         |
| ⌥ + u       | undo                  |
| ⌥ + z       | undo                  |
| ⌥ + r       | revert complete line  |
| ⌃ + k       | del right from cursor |
| ⌃ + u       | del left from cursor  |
| ⌃ + u + u   | del complete line     |

### Shortcuts: Additional command helpers: git

| Shortcut       | Action                      | Description                                |
| -------------- | --------------------------- | ------------------------------------------ |
| ⌥ + G + C      | `git checkout {cursor}`     |                                            |
| ⌥ + g + a      | `git add {cursor}`          |                                            |
| ⌥ + g + c      | `git commit -m '{cursor}'`  |                                            |
| ⌥ + g + c + a  | `git commit -am '{cursor}'` | Git: Add tracked and commit                |
| ⌥ + g + s      | `git status -s -uno`        | Git: Short status                          |
| ⌥ + g + s + a  | `git status`                |                                            |
| ⌥ + g + p      | `git pull`                  |                                            |
| ⌥ + g + p + p  | `git push`                  |                                            |

### Shortcuts: Shell redirects

| Shortcut       | Action                                | Description                                |
| -------------- | ------------------------------------- | ------------------------------------------ |
| ⌥ + r + o      | `{your prompt} 1> {cursor}`           | redirect STDOUT                            |
| ⌥ + r + e      | `{your prompt} 2> {cursor}`           | redirect STDERR                            |
| ⌥ + r + a      | `{your prompt} >& {cursor}`           | redirect STDOUT and STDERR                 |
| ⌥ + r + o + n  | `{your prompt} 1> /dev/null {cursor}` | redirect STDOUT to /dev/null               |
| ⌥ + r + e + n  | `{your prompt} 2> /dev/null {cursor}` | redirect STDERR to /dev/null               |
| ⌥ + r + a + n  | `{your prompt} >& /dev/null {cursor}` | redirect STDOUT and STDERR to /dev/null    |

### Shortcuts: Pipe to grep

**Idea is:** (p)ipe to (g)rep

| Shortcut           | Action                                 | Description                                |
| ------------------ | -------------------------------------- | ------------------------------------------ |
| ⌥ + p + g          | `{your prompt} \| grep '{cursor}'`     | pipe to grep                               |
| ⌥ + p + g + e      | `{your prompt} \| grep -E '{cursor}'`  | pipe to grep -E (using regexps)            |
| ⌥ + p + g + v      | `{your prompt} \| grep -E '{cursor}'`  | pipe to grep -v (exclude)                  |
| ⌥ + p + g + e + v  | `{your prompt} \| grep -Ev '{cursor}'` | pipe to grep -Ev (exclude using regexps)   |

### Shortcuts: Pipe to grep (at EOL)

**Idea is:** at (e)ol: (p)ipe to (g)rep

| Shortcut               | Action                                 | Description                                |
| ---------------------- | -------------------------------------- | ------------------------------------------ |
| ⌥ + e + p + g          | `{your prompt} \| grep '{cursor}'`     | pipe to grep                               |
| ⌥ + e + p + g + e      | `{your prompt} \| grep -E '{cursor}'`  | pipe to grep -E (using regexps)            |
| ⌥ + e + p + g + v      | `{your prompt} \| grep -E '{cursor}'`  | pipe to grep -v (exclude)                  |
| ⌥ + e + p + g + e + v  | `{your prompt} \| grep -Ev '{cursor}'` | pipe to grep -Ev (exclude using regexps)   |


### Shortcuts: Pipe to sed and awk

**Idea is:** 
* (p)ipe to (s)ed
* (p)ipe to (a)wk

| Shortcut           | Action                                        | Description                                |
| ------------------ | --------------------------------------------- | ------------------------------------------ |
| ⌥ + p + s          | `{your prompt} \| sed -re 's\|{cursor}\|\|'`  | pipe to sed for replacing using regexps    |
| ⌥ + p + s + t      | `{your prompt} \| sed -n  '/^{cursor}/,/^/p'` | pipe to sed to extract between two TOKENs  |
| ⌥ + p + a          | `{your prompt} \| awk '{print {cursor}}'`     | pipe to awk to print specific column       |
| ⌥ + p + a + n      | `{your prompt} \| awk NF{cursor}`             | pipe to awk to delete empty lines          |

### Shortcuts: Pipe to sed and awk (at EOL)

**Idea is:** 
* at (e)ol: (p)ipe to (s)ed
* at (e)ol: (p)ipe to (a)wk

| Shortcut               | Action                                        | Description                                |
| ---------------------- | --------------------------------------------- | ------------------------------------------ |
| ⌥ + e + p + s          | `{your prompt} \| sed -re 's\|{cursor}\|\|'`  | pipe to sed for replacing using regexps    |
| ⌥ + e + p + s + t      | `{your prompt} \| sed -n  '/^{cursor}/,/^/p'` | pipe to sed to extract between two TOKENs  |
| ⌥ + e + p + a          | `{your prompt} \| awk '{print {cursor}}'`     | pipe to awk to print specific column       |
| ⌥ + e + p + a + n      | `{your prompt} \| awk NF{cursor}`             | pipe to awk to delete empty lines          |

