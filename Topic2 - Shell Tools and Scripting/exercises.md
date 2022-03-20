### exercise 1
```shell
~: man ls
~: ls -ahlt --classify --color
```

### exercise 2
macro.sh
```shell
marco () {
    cached_path=$(pwd)
}
```

polo.sh
```shell
polo () {
    cd $cached_path
}
```

### exercise 3
fails_rarely.sh
```shell
n=$(( RANDOM % 100 ))

if [[ n -eq 42 ]]; then
    echo "Something went wrong"
    >&2 echo "The error was using magic numbers"
    exit 1
fi

echo "Everything went according to plan"
```

debug.sh
```shell
#!/usr/bin/env bash

count=0
> $2/std_out.txt
> $2/std_err.txt

if [[ ! -x $1 ]]
    then 
        echo "file should be executable!"
        exit 1
fi

while $1 1>>$2/std_out.txt 2>>$2/std_err.txt;
do
    count=$(( ${count} + 1 ))
done

echo "output message:"
cat $2/std_out.txt
echo "error message:"
cat $2/std_err.txt
echo "total successes before fail:"
echo $count
```

### exercise 4
```shell
~: find ./ -name '*.html' | xargs -d $'\n' zip htmls.zip
```

### exercise 5
sort_files.sh
```shell
#!/usr/bin/env bash

find $1 -name "*" -printf "%T@|%Tc %p\n" | sort -t'|' -n -r | cut -d'|' -f2
```
