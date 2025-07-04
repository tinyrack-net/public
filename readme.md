# WIP


```bash
curl -fL https://get.k3s.io | \
sh -s - server \
  --cluster-init \
  --cluster-cidr=10.55.0.0/16 \
  --service-cidr=10.56.0.0/16 \
  --tls-san "$(tailscale ip -4)" \
  --tls-san "127.0.0.1"
```

```bash
flux bootstrap github \
  --owner=tinyrack94 \
  --repository=public \
  --branch=main \
  --path=./clusters/production \
  --owner=tinyrack-net
```