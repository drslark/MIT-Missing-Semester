### quotes
```shell
~: foo=bar

# single-quotes
~: echo '${foo}'
${foo}

# double-quotes
~: echo "${foo}"
bar
```

### special variables
```shell
# entire last command
~: ls /root
ls: cannot open directory '/root': Permission denied
~: sudo !!
~: sudo ls /root
[sudo] password for user:
.  ..  .bash_history  .bashrc  .motd_shown  .profile

# last argument from the last command
~: mkdir folder
~: cd $_
~/folder >>> 

# report error by error code
~: grep foo bar.sh
~: echo $?
1

# error code of true/false is always 0/1
~: false
~: echo $?
1
```

### substitution
```shell
# command substitution
~: echo $(cd ..; pwd; cd ~)
/home

# process substitution
~: cat <(cd ..; pwd; cd ~) > >(tee path.txt)
/home
```

### test
```shell
# test command
~: [ a = a ] && echo ""a equals a
a equals a

# test construct
~: [[ 5 -eq 05 ]] && echo "5 equals 05"
5 equals 05

```

### globbing
```shell
# Wildcards * (multiple) and ? (single)
# Curly braces {} (enumerate)
# e.g. {foo,bar}/{a..h} makes a Cartesian Product
```

### run command in shebang
example.py
```shell
#!/usr/bin/env python
...
```

### command usages
```shell
# examples of commands
~: tldr convert
```

### find files
```shell
# find files and execute commands
~: find . --path '**/foo' --exec cat {} \;
foo
```

### find codes
```shell
# print context before and after
~: grep -C center foo
border
center
border

# invert the match
~: grep -v center foo
border
border

# find recursively
~: grep -R center
foo:center
bar:center

# find history shell commands. e.g. Ctrl + R
```
