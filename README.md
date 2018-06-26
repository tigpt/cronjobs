[![](https://images.microbadger.com/badges/image/tigpt/cronjobs.svg)](https://microbadger.com/images/tigpt/cronjobs "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/tigpt/cronjobs.svg)](https://microbadger.com/images/tigpt/cronjobs "Get your own version badge on microbadger.com")
# cronjobs
Docker alpine with curl for cronjobs

Simple image of Alpine with curl to run my cronjobs

To use it, create a docker-compose.yml with:

```
version: '3'
  services:
    cronjobs:
    restart: unless-stopped
    image: tigpt/cronjobs
    container_name: cronjobs
    volumes:
      - ./volumes/root:/etc/crontabs/root
```

put in ./volumes/root:/etc/crontabs/root folder your cronjobs

For more info on alpine cron: http://www.jimpryor.net/linux/dcron.html
