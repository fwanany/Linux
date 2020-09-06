在Linux系统中有两种不同类型的文件链接：

* 符号链接（symbolic link）

  ```
  #ls -i data_file
  -rw-r--r-- 1 root root 14 Sep 6 20:20 data_file
  #
  #ln -s data_file sl_data_file
  #
  #ls -l *data_file
  -rw-r--r-- 1 root root 14 Sep 6 20:20 data_file
  lrwxrwxrwx 1 root root  9 Sep 6 20:04 sl_data_file -> data_file
  #
  #ls -i *data_file
  #169 data_file 168 sl_data_file
  ```

* 硬链接（hard link）

  ```
  #ls -l code_file
  -rw-r--r-- 1 root root 14 Sep 6 20:11 code_file
  #
  #ln code_file hl_code_file
  #
  ls -li *code_file
  171 -rw-r--r-- 2 root root 14 Sep 6 20:11 code_file
  171 -rw-r--r-- 2 root root 14 Sep 6 20:11 hl_code_file
  #
  ```

只能对处于同一存储媒体的文件创建硬链接。要想在不同存储媒体文件之间创建链接，只能使用符号链接。