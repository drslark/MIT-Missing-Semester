### whitespace
```shell
# argument with whitespace
~: echo Hello\ World
Hello World
~: echo "Hello World"
Hello World
```

### change directory
```shell
# change to the previous directory
~: cd /home
/home >>> cd -
~: cd -
/home >>>
```

### root
```shell
# execute one command as root
~: ls /root
ls: cannot open directory '/root': Permission denied
~: sudo ls /root
[sudo] password for user:
.  ..  .bash_history  .bashrc  .motd_shown  .profile

# switch to a root terminal
~: sudo su
[sudo] password for user:
root ~ #
```
