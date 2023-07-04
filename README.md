# Docker

* Build dev container

```sh
sudo sysctl -w net.ipv6.conf.all.forwarding=1 # Use when you have IPv6 network issues
export CR_PAT=(pass show ghcr)
echo $CR_PAT | docker login ghcr.io -u devsecfranklin --password-stdin
docker build -t build-env .
docker run -it build-env sh -l
```

![Beastie](/images/beastie.png?raw=true)
