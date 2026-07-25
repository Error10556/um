# Edit typos in bash commands

Just type `um` and edit the command.

Use `um-edit -h` to learn more.

## Requirements

Bash and a terminal text editor. Vim is the default.

## Installation

You will need `curl` for the third step.

```bash
cd
mkdir -p ~/.local/bin
curl -SLo ~/.local/bin/um-edit https://raw.githubusercontent.com/Error10556/um/refs/heads/main/um-edit
chmod +x ~/.local/bin/um-edit
printf $'\n%s\n' "alias um=\"um-edit \\\"\\\$(history -p '\!\!')\\\"\"" >>.bashrc

# If ~/.local/bin is not in PATH,
printf $'%s\n' 'PATH="$PATH:$HOME/.local/bin"' >>.bashrc
```
