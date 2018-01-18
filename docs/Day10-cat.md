# cat命令

- cat命令的用途是连接文件或标准输入并打印，常用来显示文件内容或者将几个文件连接起来显示或者从标准输入读取内容并显示。它常与重定向符号配合使用。

## 1.命令格式:
  - cat[选项][文件]...

## 2.命令功能:
  - cat主要有三大功能:
    - 1. 一次显示整个文件: cat filename
    - 2. 从键盘创建一个文件: cat > filename 只能创建新文件不能编辑已有文件
    - 3. 将几个文件合并为一个文件: cat file1 file2 > file

## 3. 命令参数:
  - -A --show-al 等价于 -vET
  - -b --number-nonblank 对非空输出行编号
  - -e  等价于 -vE
  - -E --show-ends 在每行结束处显示$
  - -n --number 对输出所有行编号由1开始对所有输出的行数编号
  - -s --squeeze-blank 有连续两行以上的空白行就代换为一行的空白行
  - -t 与 -vT等价
  - -T --show-tabs 将跳格字符显示为^1
  - -u 被忽略
  - -v --show-nonprinting 使用 ^ 和 M- 引用除了LFD和TAB之外

## 4. 使用实例:
  - 实例一: 把log1.log的文件内容加上行号后输入到 log2.log这个文件中
    - 命令
      - cat -n log1.log log2.log

  - 实例二: 将log1.log 和log2.log 的文件内容加上行号(空白行不加)之后将内容附加到log.log中
    - 命令
      - cat -b log1.log log2.log log.log
  
  - 实例三: tac(反向列示) 他的功能就跟cat相反，cat是由第一行到最后一行连续显示在荧幕上，而tac则是由最后一行到第一行反向在荧幕上显示出来
    - 命令
      - tac log.txt