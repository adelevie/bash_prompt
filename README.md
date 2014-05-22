bash_prompt
===========

simple bash prompt for fun and profit

```sh
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\w\$(parse_git_branch) $ "
```
