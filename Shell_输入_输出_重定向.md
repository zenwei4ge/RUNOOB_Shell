重定向命令列表如下：
                command > file	将输出重定向到 file。
                command < file	将输入重定向到 file。
                command >> file	将输出以追加的方式重定向到 file。
                n > file	将文件描述符为 n 的文件重定向到 file。
                n >> file	将文件描述符为 n 的文件以追加的方式重定向到 file。
                n >& m	将输出文件 m 和 n 合并。
                n <& m	将输入文件 m 和 n 合并。
                << tag	将开始标记 tag 和结束标记 tag 之间的内容作为输入。
输出重定向
                实例
                        $echo   "菜鸟">users
                        $cat users
                        菜鸟教程：www.runoob.com
                        $
                        #如果不想文件被覆盖，可使用>>,在文件末尾追加
输入重定向
               实例
重定向深入讲解
               每个 Unix/Linux 命令运行时都会打开三个文件
                              标准输入文件(stdin)：stdin的文件描述符为0，Unix程序默认从stdin读取数据。
                              标准输出文件(stdout)：stdout 的文件描述符为1，Unix程序默认向stdout输出数据。
                              标准错误文件(stderr)：stderr的文件描述符为2，Unix程序会向stderr流中写入错误信息。
                command > file 将 stdout 重定向到 file，command < file 将stdin 重定向到 file。
                如果希望 stderr 重定向到 file        $ command 2 >> file
                对 stdin 和 stdout 都重定向        $ command < file1 >file2
                Here Document
                                    用来将输入重定向到一个交互式 Shell 脚本或程序
                                    语法：
                                              command << delimiter
                                                  document
                                              delimiter
                                               #将两个 delimiter 之间的内容(document) 作为输入传递给 command
                                     实例
                                             #计算行数
                                             $wc -l<< EOF
                                                 欢迎来到
                                                菜鸟教程
                                                www.runoob.com
                                            EOF
                                            #也可以将 Here Document 用在脚本中
                                            #!/bin/bash
                                            # author:菜鸟教程
                                            # url:www.runoob.com

                                            cat << EOF
                                            欢迎来到
                                            菜鸟教程
                                            www.runoob.com
                                            EOF
/dev/null 文件
             执行某个命令，但又不希望在屏幕上显示输出结果，那么可以将输出重定向到 /dev/null
             $ command > /dev/null
             
