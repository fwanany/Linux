`mv` 命令可以将文件和目录移动到另一个位置或重命名。

```
#ls -li data_one
172 -rw-r--r-- 1 root root 0 Sep 6 21:27 data_one
#
#mv data_one data_two
#
#ls -li data_two
172 -rw-r--r-- 1 root root 0 Sep 6 21:27 data_two
```

`mv` 只会改变文件和目录的名称和位置，不会改变其他信息。