有一天，当我需要用到`cURL`的时候，遭遇了如下问题：
```
PHP Startup:Unable to load dynamic library
`D:/wamp/bin/php/php5.3.13/ext/php_curl.dll` - 
应用程序无法启动, 因为应用程序的并行配置不正确. 
有关详细信息, 请参阅应用程序事件日志, 或使用命令行 sxstrace.exe 工具. 
```

百思不得其解，最好的利器就是[google][g]，最有可能的就是本身你的`php_curl.dll`就是错误的,不必多想下载新库替换之，试试更健康，这里有[各种版本][curl]，留下我自己的对应版本。

[g]: https://www.google.com
[curl]:http://www.anindya.com/php-5-4-0-x64-64-bit-for-windows/