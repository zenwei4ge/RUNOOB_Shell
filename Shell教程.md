Shell概念
            Shell 是一个用 C 语言编写的程序，它是用户使用 Linux 的桥梁
            Shell 是指一种应用程序，这个应用程序提供了一个界面，用户通过这个界面访问操作系统内核的服务。
 Shell 环境
            要有一个能编写代码的文本编辑器和一个能解释执行的脚本解释器
            常见的有：
                        Bourne Shell（/usr/bin/sh或/bin/sh）
                        Bourne Again Shell（/bin/bash）
                        C Shell（/usr/bin/csh）
                        K Shell（/usr/bin/ksh）
                        Shell for Root（/sbin/sh）
第一个shell脚本
            打开文本编辑器，新建test.sh
                  #!/bin/bash     //指定Shell
                  echo "Hello World!"  //输出文本
运行 Shell 脚本两种方法：   
          1、作为可执行程序
                            ①将上面的代码保存为 test.sh，并 cd 到相应目录：
                            ②chmod +x ./test.sh  #使脚本具有执行权限
                            ③./test.sh  #执行脚本
          2.作为解释器参数
                            /bin/sh test.sh
          
                           
                      
