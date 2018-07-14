# vue-sell
Vue.js 高仿饿了么外卖 App 课程源码

本源码基于 GPL 协议，仅用于 Vue 实战项目的学习，不可作为商业用途。

主要为了对接“weixin-sell-backend”后台


# 接口配置
在/config/index.js文件里配置

# nginx的server配置

    server {
        listen       80;
        #server_namet,添前端项目域名地址  
        server_name  vya8m7.natappfree.cc;
        
        access_log D:\\nginx\\nginx-1.13.8\logs\access.log combined;
        location / {
            root   D:\wamp64\www\sell;
            index  index.html index.htm;   
        }
        
        location /sell/ {
            proxy_pass http://127.0.0.1:8080/;     
        }
        
         error_page   500 502 503 504  /50x.html;
         location = /50x.html {
              root   html;    
         }
    }



