# appium-ui
[![Build Status](https://travis-ci.org/bongster/appium-ui.svg?branch=master)](https://travis-ci.org/bongster/appium-ui)

### REQUIREMENTS
* docker
* docker-compose

### HOW TO USE

* docker-compose up - (start services)
* docker-compose down - (down services)

### SERVICES

* frontend

> The service for showing user about result data about test

  - PORTS: 3000
  - URL: http://localhost:3000

* rabbitmq

> Queue

  - PORTS: 15672, 5672
  - URL: http://localhost:15672
  - USER: rabbitmq
  - PASSWORD: rabbitmq

### Tip

* Add this script in your env for fix up your branch

```
function gitclean() {
    git pull
    git branch --merged master | grep -v "\master" | xargs -n 1 git branch -d
    git remote prune origin
    git gc
}
```
