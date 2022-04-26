# 关于本项目
本项目由[WoL](https://github.com/WoLeo-Z)编写，基于PHP开发，实现网页代理的功能。
更多请看我博客的文章：[PHP-Proxy网页代理](https://blog.wol1.cf/index.php/archives/101/)。

# 食用方法
1. 下载源码并解压到网站根目录。
2. 编辑伪静态规则：
Nginx：
`if ( !-e $request_filename) {rewrite ^/(.*)$ /index.php?$1 last;break;}`
Apache：
`RewriteRule '^/(.*)$$' /index.php?$1 [L] `

4. `index.php` 外链、外链图片、外链静态文件等请求不通过`PHP-Proxy`，地址栏不会显示目标域名.
5. `index1.php` 传统版，地址栏会显示目标域名，**性能不及前者**。所有外链、外链图片、外链静态文件等请求都通过`PHP-Proxy`。
6. 两个文件请按照个人喜好自行选择。

# 功能
- 密码访问（默认为`PHP-Proxy`）
- 若PHP空间在国外，基本可代理所有网站。
- 支持`Cookies`,`Headers`,`Post请求`等。

# To Do List
- `index_all` 代理所有外链、外链图片、外链静态文件，但地址栏不显示目标域名。
- 支持`Delete`,`Put`,`Patch`等请求方法。
- 管理后台 `/admin`

# 参考
[yitd/Any-Proxy](https://github.com/yitd/Any-Proxy)
