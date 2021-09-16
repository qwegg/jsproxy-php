# jsproxy-php

## 宝塔面板食用 php 版 jsproxy

Nginx 设置伪静态
```
if (!-f $request_filename){
	set $rule_0 1$rule_0;
}
if (!-d $request_filename){
	set $rule_0 2$rule_0;
}
if ($rule_0 = "21"){
	rewrite ^/?http/(.*?)/?$ /jsproxy/index.php?url=$1 last;
}
```
**Apache**  
.htaccess 伪静态, 普通虚机可用

## 起飞 ##
https://__DOMAIN__/jsproxy/404.html
