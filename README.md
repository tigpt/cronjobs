# cronjobs
Docker alpine with curl for cronjobs

Simple image of Alpine with curl to run my corncobs

To use it, create a docker-compose.yml with:

```
version: '3'
  services:
    cronjob:
    restart: unless-stopped
    image: tigpt/cronjob
    container_name: cronjob
    volumes:
      - ./volumes/root:/etc/crontabs/root
```

put in ./volumes/root:/etc/crontabs/root folder your cronjobs

For more info on alpine cron: http://www.jimpryor.net/linux/dcron.html
