# psychology-xingyu-website

## 更新SSL证书
1. 腾讯云下载证书（1_xingyuxinli.com_bundle.crt为公钥，2_xingyuxinli.com.key为私钥）
2. SCP下载的证书到服务器ubuntu用户目录下的website-cert目录：

```
scp 1_xingyuxinli.com_bundle.crt ubuntu@118.24.36.172:~/website-cert/xingyuxinli-public.crt
scp 2_xingyuxinli.com.key ubuntu@118.24.36.172:~/website-cert/xingyuxinli-private.key
```

3. SSH到服务器，执行命令：
```
cd psychology-xingyu-website
sudo ./build-and-run.sh
```

4. 检查网站是否访问正常，且证书更新正常
