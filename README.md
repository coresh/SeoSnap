![logo](https://github.com/experius/SeoSnap/raw/master/assets/logo.png)

Setup for the whole seosnap stack including dashboard, cache server and cache warmer used for prerendering and full
 page caching PWA's.
 
# Installation
* Pull the repo
```
git clone --recursive git@github.com:experius/SeoSnap.git
```
* **IMPORTANT** Update .env file admin username and password. (These have a value default value)
* Start, build and stop the container
```
docker-compose up --build -d && docker-compose down
```

# Usage
* Dashboard: http://127.0.0.1:8080/ (default login: snaptron/Sn@ptron1337)
* API Docs: http://127.0.0.1:8080/docs
* PHPMyAdmin: http://127.0.0.1:8081/
* Cache Server: http://127.0.0.1:5000/render/\<your url\>

Logs directory ./logs

Cache directory ./cache

## Run cache warmer
Make sure you have created a website via dashboard http://127.0.0.1:8080/seosnap/website/add/
```
docker-compose run cachewarmer <website id>
```