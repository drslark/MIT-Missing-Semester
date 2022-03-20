### exercise 1
```shell
~: echo $SHELL
/usr/bin/zs
```

### exercise 2
```shell
~: mkdir /tmp/missing
```

### exercise 3
```shell
~: man touch
```

### exercise 4
```shell
~: touch /tmp/missing/semester
```

### exercise 5
```shell
~: echo '#!/bin/sh'"\n"'curl --head --silent https://missing.csail.mit.edu' > /tmp/missing/semester
```

### exercise 6
```shell
~: ls -l /tmp/missing/semester
-rw-r--r-- 1 user user 61 Mar 19 12:28 /tmp/missing/semester
```

### exercise 7
```shell
~: cd /tmp/missing/semester; sh semester; cd -;
```

### exercise 8
```shell
~: man chmod
```

### exercise 9
```shell
~: chmod u+x /tmp/missing/semester
```

### exercise 10
```shell
~: cd /tmp/missing/;./semester | grep last-modified > ~/last-modified.txt; cd -;
```

### exercise 11
```shell
~: cat /sys/class/power_supply/BAT1/capacity_level
```