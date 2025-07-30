# Clia - CLI Assistant
🔧 Ask Linux command-line questions and get the command and simplified help answers from your local Ollama model — right from your terminal.
---

A minimalist Bash tool that lets you ask Linux-related command-line questions directly from your terminal and get expert, copy-paste-ready answers powered by your local [Ollama](https://ollama.com/) server.

I made it to avoid context-switching, having to move away from the terminal to search for a command help query. Feel free to propose suggestions and improvements.

## ✨ Features

- Get terminal commands and clear explanations from LLMs like LLaMA, Mistral, etc.
- Optional interactive mode (no quotes needed)
- Change models via `-m` flag
- Respects `OLLAMA_DEFAULT_MODEL` environment variable
- Checks and offers to pull models if not already installed

## 🖥️ Example

```bash
$ clia How do I create a tar.gz archive excluding .git and node_modules folders?

`tar -czvf archive.tar.gz --exclude=.git --exclude=node_modules 
/path/to/directory`

1. `tar`: This command is used to create archives of files on the 
file system.
2. `-c`: Create (create a new archive).
3. `-z`: Compress the archive with gzip (creates .gz extension).
4. `-v`: Verbose mode, which displays each file as it's added to the 
archive.
5. `-f`: Specify the output file name for the archive.
6. `archive.tar.gz`: Specifies the file name of the archive that is 
created.
7. `--exclude `.git`: Excludes all files and directories in the 
`.git` directory from being included in the archive.
8. `--exclude=node_modules`: Excludes all files and directories in 
the `node_modules` directory from being included in the archive.
9. `/path/to/directory`: Specifies the path to the directory that 
you want to include in the archive.


```

## 🔧 Requirements

* [Ollama](https://ollama.com/)  installed and running locally
* Bash or compatible shell

## 🧪 Quick Start

```
# 1. Create bin dir to store the tool
mkdir -p ~/bin

# 2. Download the script
curl -fsSL -o ~/bin/clia https://raw.githubusercontent.com/Mircea-S/clia/main/clia

# 3. Make it executable
chmod +x ~/bin/clia

# 4. Add to ~/.bashrc (or ~/.zshrc if using Zsh)
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc
echo 'export OLLAMA_DEFAULT_MODEL=llama3.2' >> ~/.bashrc

# 5. Reload shell
source ~/.bashrc
```

