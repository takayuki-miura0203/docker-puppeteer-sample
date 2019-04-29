# docker-puppeteer-sample
sample code of puppeteer on docker

## environment
everywhere only if docker is enabled.

## exec
### using docker only
```
docker run -i --init --rm --cap-add=SYS_ADMIN \
   --name puppeteer-chrome puppeteer-chrome-linux \
   node -e "`cat /path/to/puppeteer/app/main.js`"
```

### using docker-compose
1. change the `/path/to` path to your real path

2. exec below
```
docker-compose run --rm --entrypoint /bin/sh puppeteer
```

3. in docker process, exec below
```
node main.js
```

## reference
### puppeteer/troubleshooting.md at master · GoogleChrome/puppeteer
https://github.com/GoogleChrome/puppeteer/blob/master/docs/troubleshooting.md

### Dockerで日本語対応のHeadless Chrome + puppeteerを立ち上げ
https://morizyun.github.io/docker/docker-compose-chrome-puppeteer-headless.html#%E8%A3%9C%E8%B6%B3%EF%BC%9Apuppeteer%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9
