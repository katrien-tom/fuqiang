# clash_rules
clash rules
一键设置镜像加速
修改文件 `/etc/docker/daemon.json`（如果不存在则创建）

```shell
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://doc.binggao.xyz"]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
```

支持Docker

```
docker build --tag 'sing-box' .
docker run -d -p 5000:5000 --name singbox sing-box:latest
```