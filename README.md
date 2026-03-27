# immich-stack

This repository contains the GitOps-driven configuration for my Immich deployment. It is designed to be managed and deployed via Portainer.

## Environment Setup
The stack relies on the following environment variables (defined in Portainer's Stack UI):

| Variable | Description | Default/Example |
| :--- | :--- | :--- |
| `DB_HOSTNAME` | Database container name | `postgres` |
| `DB_USERNAME` | Postgres user | `immich` |
| `DB_PASSWORD` | Postgres password | `(Defined in Secrets)` |
| `DB_NAME` | Database name | `immich` |

## Persistent Storage
I use bind mounts for data persistence. Ensure these paths exist on the Docker host:
* `/opt/docker/immich/upload` - Original photos and videos
* `/opt/docker/immich/cache` - Thumbnails and ML cache
* `/opt/docker/immich/postgres` - Database files

---

[Back to Homelab Overview](https://github.com/KubaMichalowski-homelab)
