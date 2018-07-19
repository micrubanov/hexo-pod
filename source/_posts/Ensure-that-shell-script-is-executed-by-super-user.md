---
title: Ensure that shell script is executed by super user
date: 2018-07-19 03:06:56
tags:
---

```

# $EUID is shell env variable name that hold an id value of it's "owner".
# those whom are greater than 0, are non root's.

if [[ $EUID -gt 0 ]]; then
        echo "Please run as root/sudo"
        exit 1
fi


```
