# inspires
This is a test .
test for branches


LLDB:
image lookup -a 表达式、image list
查找某个函数：
对于有调试符号的这样使用
image lookup -r -n <FUNC_REGEX>
对于无调试符号的这样使用：
image lookup -r -s <FUNC_REGEX>

memory read 0x35f1c 0x35f46 -outfile /tmp/test.txt  // 将内存区域保存到文件
默认情况下，memory read 只能读取 1024字节数据 
解决方法：加－force参数
memory read 0x1000 0x3000 -outfile /tmp/test.txt -force
或者:
memory read 0x1000 -outfile /tmp/test.txt -count 0x2000 -force
memory read $x0(寄存器) -outfile /tmp/test.txt -count 0x2000 -force

memory read 0x1000 0x3000 -outfile /tmp/test.bin --binary -force //二进制输出

mac os :
调试进程target create "/bin/ls"

条件断点:
br s -a 0x02107730+0x000ab000 -c ‘(BOOL)[(NSString *)$r2 isEqualToString:@”snakeninny”]’

cycript:


class-dump:
class-dump –list-arches AlipayWallet.decrypted
class-dump -S -s -H WeChat_armv7.decrypted -o dumparmv7 
class-dump -s -S -H –arch armv7 AlipayWallet.decrypted -o dumpAlipay 

