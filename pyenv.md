# Installing pyenv

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| Install Homebrew (if not already installed)     | `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"` |
| Install Pyenv with Homebrew                     | `brew install pyenv`                    |
| Open .zshrc or .bash                            | ` nano ~/.bash_profile ` or `nano ~/.zshrc `
| Add Pyenv to your shell (bash or zsh)           | [Scripts below](#script)  |
| Restart your shell or run                       | `source ~/.bash_profile` (or `source ~/.zshrc` for Zsh) |
| Verify Pyenv installation                       | `pyenv --version`                        |
| View Available versions for Pyenv               | `pyenv install --list`                        |
| Install pythibg version from the list above     | `pyenv install 3.9.10`                        |
| Check on the installed pyenv                    | `pyenv versions` |

<br>

# Basic Usage

| Description                                     | Command                                  |
|-------------------------------------------------|------------------------------------------|
| Switch the gloabl Python to specific version    | `pyenv global 3.9.10 ` and then do `python -V` |
| Switch back to system                           | `pyenv global system`                    |
| Create virtual Env                              | `pyenv virtualenv [python version] [env-name]` |
| Activate virtual Env                            | `pyenv activate [env-name` |
| Check on the installed pyenv virtualenv         | `pyenv virtualenvs`|


<br>

 <a name="script"></a>
 ### Zsh Script
 Add the fllowing lines to the end of the .zshrc file in your root directory (~) 
 
 ```export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
export PIPENV_PYTHON="$PYENV_ROOT/shims/python"

plugin=(
  pyenv
)

eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```
<hr>

 ### Bash Script
 Add the fllowing lines to the end of the .bash file in your root directory (sudo nano ~/.bashrc)
 
 ```
export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile 
if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bash_profile

```
