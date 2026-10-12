# readarr-swarm

E-book management for *arr ecosystem.

## Stack

- **Host**: ore-dock-110-1
- **Stack**: `readarr-swarm`
- **Image**: linuxserver/readarr:0.4.19-nightly
- **Config**: named volumes `readarr-swarm.config`, `readarr-swarm.db`

## Ports

| Port | Published | Protocol |
|------|----------|----------|
| 8787 | 8787 | TCP |

## Deploy

```bash
ssh ore-dock-110-1
cd /data/compose/readarr-swarm
set -a && source .env && docker stack deploy -c docker-compose.yml --with-registry-auth readarr-swarm && set +a
```
