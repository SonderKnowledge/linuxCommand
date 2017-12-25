# ls命令

* ls命令是linux下最常用的命令，ls命令就是list的缩写，ls用来打印当前目录的清单。通过ls命令不仅可以查看linux文件夹包含的文件而且还可以查看文件权限(包括目录、文件夹、文件权限)等。

* 1.命令格式:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ls[选项][目录名]
* 2.命令功能:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;列出目标目录中所有的子目录和文件
* 3.常用参数:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -a, -all 列出目录下的所有文件，包括以'.'开头的隐含文件   
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
  -A同-a,但是不列出'.'(表示当前目录)和'..'(表示当前目录的父目录)  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -c配合 -lt: 根据ctime排序及显示 ctime(文件状态最后更改的时间)配合 -i: 显示 ctime 但根据名称排序,否则根据 ctime 排序  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -C 每栏由上至下列出项目  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -color[=WHEN]控制是否使用色彩分辨文件,WHEN可以是 'never'、'always'、'auto'其中之一  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -d, -directory将目录像文件一样显示而不是显示其下的文件  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -D, -dired 产生适合Emacs的dired模式使用的结果  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -f对输出的文件不进行排序,-aU选项生效, -lst选项失效  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -g 类似 -l,但不列出所有者  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -G, -no-group 不列出任何有关组的信息  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -h, -human-readable 以容易理解的格式列出文件大小(例如 1K 234M 1G)  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  -si 类似 -h,但文件大小取 1000 的次方而不是 1024