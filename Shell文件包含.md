语法格式
          . filename   # 注意点号(.)和文件名中间有一空格

            或

            source filename
 实例
          #在test2.sh文件中引用test1.sh文件
          . ./test1.sh
          #包含文件代码
          source ./test1.sh
         为 test2.sh 添加可执行权限并执行：
                 #test1.sh不需要执行权限
                 $ chmod +x test2.sh 
                  $ ./test2.sh 
