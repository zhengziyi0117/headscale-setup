# 基本使用
```sh
git clone https://github.com/zhengziyi0117/headscale-setup.git
```
在git clone下来后，需要修改caddy-config和headscale-config和docker-compose.yml
主要工作为替换域名，将里面的`ziyiziyi.online`替换为自己对应的域名
这些是需要修改的地址
- caddy-config/Caddyfile的反向代理的域名地址
- headscale-config/config.yaml中的`server_url`
- headscale-config/derp.yaml里面的hostname字段以及ipv4字段
- docker-compose.yml中derp service的`DERP_DOMAIN`环境变量的域名地址

这个项目主要参考这个仓库搭建: https://github.com/xpzouying/headscale
提供快速搭建headscale server的功能