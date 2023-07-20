# Linux Command
## `cat`
`cat` 是一个在 Unix 或类 Unix 操作系统中常用的命令，用于查看文件内容或将多个文件合并输出到标准输出。
### 语法
1. 查看文件内容：
```shell
cat file.txt
```
2. 合并文件：
```shell
cat file1.txt file2.txt > merged.txt
```
3. 追加文件：
```shell
cat file1.txt >> file2.txt
```
4. 显示行号：
```shell
cat -n file.txt
```

## `bash/sh`
`bash/sh`用于执行shell脚本。
### 语法
```shell
bash/sh script.sh
```

## `du`
du命令用于显示目录或文件所占用的磁盘空间。
### 语法
1. 显示目录或文件所占用的磁盘空间：
```shell
du -h file.txt
```
2. 显示当前文件夹大小：
```shell
du -sh
```
-s参数表示显示总大小，-h表示以人类可读的方式显示。

## nvidia
### `nvidia-smi`
`nvidia-smi`用于查看GPU使用情况，包括显卡驱动版本，以及有多少块显卡、使用情况如何等。
#### 语法
```shell
nvidia-smi
```
### nvtop
`nvtop`可以实时显示GPU使用情况，包括GPU使用率、显存使用率、显存使用量等。按Ctrl+C退出。
#### 语法
```shell
nvtop
```

## `>`
`>`用于将命令的输出重定向到文件。
### 语法
```shell
command > file.txt
```
