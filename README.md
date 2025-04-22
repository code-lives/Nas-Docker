# docker-compose 部署好玩的镜像(极空间)

## qbittorrent

```ymal
version: '3'
services:
  qbittorrent:
    image: linuxserver/qbittorrent:4.5.2
    container_name: qbittorrent
    restart: unless-stopped
    ports:
      - "6881:6881"
      - "6881:6881/udp"
      - "8083:8083"
    environment:
      - PUID=1000
      - PGID=1000
      - TZ=Asia/Shanghai
      - WEBUI_PORT=8083
    volumes:
      - /tmp/zfsv3/sata11/****/data/docker/qbittorrent/config:/config
      - /tmp/zfsv3/sata11/****/data/docker/qbittorrent/downloads:/downloads

```

### 磁力链接 （供参考）

```javascript
magnet:?xt=urn:btih:c04585d960ae08cc7509783cf984a097f908c0f3&dn=%e5%bf%a0%e7%8a%ac%e5%85%ab%e5%85%ac%e7%9a%84%e6%95%85%e4%ba%8b.Hachiko%20A%20Dogs%20Story.2009.BluRay.1080p.HEVC.AC3.%e4%b8%ad%e8%8b%b1%e7%89%b9%e6%95%88-DiaosMan%40Bger
```
