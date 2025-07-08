### Nginx原版

```
localtion / {
      try_files $uri $uri =404;
}
```

### 改版后

```
location / {
     # 由原来的404，改成指定index.html
     try_files $uri $uri /index.html;  
}
```