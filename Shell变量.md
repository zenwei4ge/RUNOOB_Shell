命名
        命名只能使用英文字母，数字和下划线，首个字符不能以数字开头，不能使用bash里的关键字
使用变量
         使用一个已定义的变量，前面加美元符$
         示例
                  your_name="qinjx"
                  echo $your_name
                  echo ${your_name}
只读变量
            使用readonly可将变量定义为
            实例
                    #!/bin/bash
                    myUrl="http://www.w3cschool.cc"
                    readonly myUrl
 删除变量
            使用 unset 命令
            语法
                  unset variable_name
             unset 命令不能删除只读变量
 变量类型
              1.局部变量  仅在当前Shell实例有效
              2.环境变量  所有程序都能访问
              3.shell变量
  Shell字符串
              单引号
                      限制    单引号字符串中的变量是无效的
                              单引号字串中不能出现单引号（对单引号使用转义符后也不行）
              双引号  
                      实例
                            your_name='qinjx'
                            str="Hello, I know your are \"$your_name\"! \n"
                      优点：双引号里可以有变量
                            双引号里可以出现转义字符
              拼接字符串
                            your_name="qinjx"
                            greeting="hello,"$your_name"!"
                            greeting1="hello,${your_name}!"
                            echo $greeting $greeting_1
               获取字符串长度
                               string="1234"
                               echo ${#string}
               提取子字符串
                               string="1234"
                               echo ${string:1:4}
                查找子字符串
                                查找字符 "i 或 s" 的位置：echo `expr index "$string" is`  # 输出 8 "`" 是反引号，而不是单引号 "'"
    Shell 数组
                  支持一维数组（不支持多维数组）
                  定义数组     数组名=(值1 值2 ... 值n)
                              单独定义各个分量
                                        array_name[0]=value0
                                        array_name[1]=value1
                  读取数组
                                ${数组名[下标]}
                                使用@符号作为下标可以获取数组中的所有元素
                  获取数组的长度
                                与获取字符串长度相同
                                        echo ${#array_name[@]}
                                        # 或者
                                        length=${#array_name[*]}
                                        # 取得数组单个元素的长度
                                        lengthn=${#array_name[n]}
  Shell 注释         每一行加一个#
                    需要注释大块内容可以用花括号括起来
                  
                                      
                  
                 
                
                            
                
