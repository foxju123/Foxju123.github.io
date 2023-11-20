# Dreamer CMS
## Dreamer CMS是一个梦想家内容管理系统。

##任意文件上传漏洞
Dreamer CMS 开源版V4.0.1 uploadFile存在任意文件上传，该漏洞源于组件/upload/uploadFile对用户请求未进行过滤，导致普通用户可以上传任意文件，攻击者可利用该漏洞通过注入精心设计的有效载荷执行任意Web脚本或HTML。

![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/ae202b56-4099-4aaa-8eda-9f18a419484e)
![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/c2b424d8-a241-4898-b380-e432228f413a)

通过查看源代码发现未对后缀进行过滤导致可以上传jsp ，如下是后台源码

![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/f71ccd5e-8eb5-47fb-b6f8-c3a1496f7d2b)

如下图片是上传成功之后的响应

![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/0946158f-fce0-4c47-96a6-d195992fe493)
