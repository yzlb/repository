# Gitbook HTML 的发布

## ubuntu 安装 nginx

安装nginx

```
sudo apt-get install nginx
```

启动nginx

```
service nginx restart
```

在写好的书的目录

```
gitgook build
```

Gitbook 会生成一个 _book 的目录，复制目录中的文件到 /var/www/html 目录,如果这个服务器上你发布的书比较多的话最好建个子目录 如 book1 .

```
cd _book
cp -r * /var/www/html/book1
```

在浏览器中打开，http://你的网站/book1,就可以浏览了。