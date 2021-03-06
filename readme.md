# docker-puppeteer-sample
Sample code of puppeteer on docker.

## environment
Everywhere only if docker is enabled.

## exec
### using docker only
```
docker run -i --init --rm --cap-add=SYS_ADMIN \
   --name puppeteer-chrome puppeteer-chrome-linux \
   node -e "`cat /path/to/puppeteer/app/main.js`"
```

### using docker-compose
1. Change the `/path/to` to real path in `docker-compose.yml` .

2. Exec below.
```
docker-compose run --rm --entrypoint /bin/sh puppeteer
```

3. In docker process, exec below.
```
node main.js
```

Because of mounted, you can modify `main.js` from your host machine.

## reference
### puppeteer/troubleshooting.md at master · GoogleChrome/puppeteer
https://github.com/GoogleChrome/puppeteer/blob/master/docs/troubleshooting.md

### Dockerで日本語対応のHeadless Chrome + puppeteerを立ち上げ
https://morizyun.github.io/docker/docker-compose-chrome-puppeteer-headless.html#%E8%A3%9C%E8%B6%B3%EF%BC%9Apuppeteer%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9

### Puppeteerがクローリングに使えそう
https://gist.github.com/sys9kdr/477d4c44b51c722331951c3f4b0b0c13
