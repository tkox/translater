### 1. 正则表达式

* 符号"."匹配除换行符"\n"之外的任何一个字符
* 符号"["和"]"共同匹配一个字符类，即方括号内只要有一个字符被匹配上，那么方括号括起来的整个表达式都被匹配上了，可以使用"-"表示一个范围，如[0-9]表示数字，如果方括号的第一个字符是"^"，则表示对这个字符类取补，即方括号内任何字符都不能被匹配上
* 符号"^"用在方括号之外则匹配一行的开头
* 符号"$"用于匹配一行的结尾
* 符号"<<EOF>>"用于匹配文件的结尾
* 符号"{"和"}"，如果花括号内包含了一个或者两个数字，则代表花括号之前的那个表达式需要出现的次数，如A{5}匹配AAAAA,A{1, 3}匹配A、AA、AAA。如果花括号之内是一个在Flex源代码的定义部分定义过的名字，则表示那个名字对应的正则表达式
* 符号"*"为Kleene闭包操作，匹配零或者多个表达式，如A*表示零个过着多个A
* 符号"+"为正闭包操作，匹配一个或者多个表达式
* 符号"?"匹配零个或者一个表达式
* 符号"|"为选择操作，匹配器之前或者之后的任一表达式
* 符号"\"用于表示各种转义字符
* 符号"""将逐字匹配被引起来的内容（无视各种特殊符号及转义字符）

