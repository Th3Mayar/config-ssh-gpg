```sudo apt update```

```sudo apt upgrade```

### prompt_segment black green '%1~'

```curl -fsSL https://fnm.vercel.app/install | bash```

```prompt_node_npm() {
  # Test if node project in directory hierarchy
  local dir="$PWD"
  while [[ ! -f "$dir/package.json" ]]; do
    [[ "$dir" = "/" ]] && return
    dir="${dir:h}"
  done

  local nodeVersion=node --version | sed -e "s/v//g"
  #local npmVersion=npm --version
  prompt_segment black green "⬢ $nodeVersion"
}
```

```source <(fnm completions --shell zsh)```

```fnm completions --shell zsh > ~/Repos/zsh-autocomplete/Completions/_fnm```

```fpath=(/home/$USER/Repos/zsh-autocomplete/Completions/_fnm $fpath)```
