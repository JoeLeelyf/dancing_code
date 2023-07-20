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

## sudo chmod
`sudo chmod`用于修改文件或目录的权限。
### 语法
```shell
sudo chmod <permisions> <file_path>
```
其中`<permisions>`是权限，三位分别代表所有者、所属组、其他人的权限，`<file_path>`是文件或目录的路径。<br>
每一位的权限可以使用以下数字表示：
- 0：没有权限
- 1：执行权限
- 2：写权限
- 3：写和执行权限
- 4：读权限
- 5：读和执行权限
- 6：读和写权限
- 7：读、写和执行权限
例如，权限设置为 755 意味着：<br>
- 所有者具有读、写和执行权限（7）<br>
- 所属组和其他用户具有读和执行权限（5）<br>

这样设置权限后，所有者可以读取、写入和执行文件，而所属组和其他用户只能读取和执行文件。<br>
同样地，权限设置为 644 意味着：
- 所有者具有读和写权限（6）
- 所属组和其他用户只能读取文件（4）

### 示例
1. 将文件的所有者权限设置为读、写和执行，所属组和其他用户权限设置为读和执行：
```shell
sudo chmod 755 file.txt
```
2. 将目录的所有者权限设置为读和写，所属组和其他用户权限设置为读：
```shell
sudo chmod 644 ./output
```

## mkdir -p
`mkdir -p`用于递归创建目录。即当父目录不存在时，会自动创建父目录。
### 语法
```shell
mkdir -p path/to/dir
```
