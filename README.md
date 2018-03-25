# vue_todo



### [nginx文件配置](https://www.cnblogs.com/yysbolg/p/7357600.html)
server
{
	listen 80;
	index index.html index.htm index.php;
	root /var/www/html/vue_todo;
	location / {
		try_files $uri $uri/ @router;
		index index.html;
	}

	location @router {
		rewrite ^.*$ /index.html last;
	}
}

