# mv命令

- mv是move的缩写可以用来移动文件或者将文件改名，是linux系统常用的命令，经常用来备份文件或者目录。

## 1.命令格式:
  - mv[选项] 源文件或目录 目标文件或目录

## 2.命令功能:
  - 视mv命令中第二个参数类型的不同(是目标还是目标目录)，mv命令将文件重命名或将其移至一个新目录中。当第二个参数类型是文件时，mv命令完成文件的重命名。此时，源文件只能有一个(也可以是源目录名)它将所给的源文件或目录重命名为给定的目标文件名。当第二个参数是已存在的目录名称时，源文件或目录参数可以有多个，mv命令将各参数指定的源文件均移至目标目录中。在跨文件系统移动文件时mv先拷贝再将原有文件删除，而链至该文件的链接也将丢失。

## 3.命令参数:
  - -b 若需覆盖文件则覆盖前先行备份
  - -f force强制的意思，如果目标文件已经存在不会询问直接覆盖
  - -i 若目标文件已经存在时，就会询问是否覆盖
  - -u 若目标文件已经存在且source比较新才会更新
  - -t --target-directory=DIRECTORY move all SOURCE arguments into DIRECTORY 既指定mv的目标目录该选项适用于移动多个源文件到一个目录的情况此时目标目录在前源文件在后。

## 4.命令实例:
  - 实例一: 文件改名
  - 命令:
    - mv test.log test1.txt
  
  - 实例二: 移动文件
    - 命令:
      - mv test1.txt test
  
  - 实例三: 将文件log1.txt, log2.txt, log3.txt移动到test中
    - 命令:
      - mv log1.txt log2.txt log3.txt test
      - 或者 mv -t /opt/soft/test log1.txt log2.txt log3.txt

  - 实例四: 将文件file1改名为file2 如果file2存在则询问是否覆盖
    - 命令:
      - mv -i file1 file2
  
  - 实例五: 将文件file1改名为file2 即使file2存在也是直接覆盖
    - 命令:
      - mv -f file1 file2
  
  - 实例六: 移动当前文件夹下的所有文件到上一级目录
    - 命令:
      - mv* ../
  
  - 实例七: 把当前目录的一个子目录里的文件移动到另一个子目录里
    - 命令:
      - mv test/*.txt test