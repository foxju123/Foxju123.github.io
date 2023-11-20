# Dreamer CMS 
### Dreamer CMS  GitHub repository address  https://github.com/iteachyou-wjn/dreamer_cms 。

## Arbitrary file upload vulnerability
Dreamer CMS open source version V4.0.1 uploadFile has arbitrary file upload vulnerability. This vulnerability is caused by the component /upload/uploadFile not filtering user requests, resulting in ordinary users being able to upload any file. Attackers can exploit this vulnerability by injecting carefully designed payloads to execute arbitrary web scripts or HTML.

![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/ae202b56-4099-4aaa-8eda-9f18a419484e)
![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/c2b424d8-a241-4898-b380-e432228f413a)

By looking at the source code, it is found that the suffix is not filtered, resulting in the possibility of uploading jsp. The following is the background source code.

![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/f71ccd5e-8eb5-47fb-b6f8-c3a1496f7d2b)



![image](https://github.com/foxju123/Foxju123.github.io/assets/40843725/0946158f-fce0-4c47-96a6-d195992fe493)
