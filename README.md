## How to run this demo project
#### initial preparation work
```
The basic development environment of Docker, Nodejs, PHP
Nodejs >= 16.13
PHP >= 7.4
npm >= 8.1.2
```
step 1. clone project
```bash
git clone git@github.com:diggex/weather-demo.git --recurse-submodules
````

step 2. build docker container 
```
cd weather-docker 
sh deploy.sh start
```

step 3. install PHP API dependencies.
```
docker exec -i weather-php /bin/bash -c "composer install"
```
After install, open http://localhost:8080/api/owners with browser or other way, check API status

step 4. build UI
```
cd weather-ui 
npm ci
npm run build
```

step 5. The browser open the http://localhost check project status.

