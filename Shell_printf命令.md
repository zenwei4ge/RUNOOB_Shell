printf 命令的语法：
             format-string: 为格式控制字符串
             arguments: 为参数列表
实例
        printf "%-10s %-8s %-4s\n" 姓名 性别 体重kg  
        printf "%-10s %-8s %-4.2f\n" 郭靖 男 66.1234 
        printf "%-10s %-8s %-4.2f\n" 杨过 男 48.6543 
        printf "%-10s %-8s %-4.2f\n" 郭芙 女 47.9876 

%d %s %c %f 格式替代符详解:
              d: Decimal 十进制整数 -- 对应位置参数必须是十进制整数，否则报错！
              s: String 字符串 -- 对应位置参数必须是字符串或者字符型，否则报错！
              c: Char 字符 -- 对应位置参数必须是字符串或者字符型，否则报错！
              f: Float 浮点 -- 对应位置参数必须是数字型，否则报错！
printf的转义序列
          \a	警告字符，通常为ASCII的BEL字符
          \b	后退
          \c	抑制（不显示）输出结果中任何结尾的换行字符（只在%b格式指示符控制下的参数字符串中有效），而且，任何留在参数里的字符、任何接下来的参数以及任何留在格式字符串中的字符，都被忽略
          \f	换页（formfeed）
          \n	换行
          \r	回车（Carriage return）
          \t	水平制表符
          \v	垂直制表符
          \\	一个字面上的反斜杠字符
          \ddd	表示1到3位数八进制值的字符。仅在格式字符串中有效
          \0ddd	表示1到3位的八进制值字符
实例
       $ printf "a string, no processing:<%s>\n" "A\nB"
        a string, no processing:<A\nB>

        $ printf "a string, no processing:<%b>\n" "A\nB"
        a string, no processing:<A
        B>

        $ printf "www.runoob.com \a"
        www.runoob.com $       
