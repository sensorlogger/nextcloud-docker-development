# SensorLogger for Nextcloud Development

Simple nextcloud docker environment. Ready to test and develop SensorLogger for nextcloud.
Created and tested for use with Ubuntu 20.04. But should work on any system supporting composer and docker.

### Requirements
* composer
    * https://wiki.ubuntuusers.de/Composer/
    * https://getcomposer.org/download/
* docker-compose
    * sudo apt-get install docker-compose

### Install
1. your@machine:$ `git clone https://github.com/alexstocker/nextcloud-docker-development.git`
2. your@machine:$ `cd nextcloud-docker-development`
3. your@machine:...nextcloud-docker-development$ `composer install`
4. your@machine:...nextcloud-docker-development$ `composer docker-up`
5. your@machine:...nextcloud-docker-development$ `sudo chown -Rf [USER]:[GROUP] sensorlogger/` (adjust [USER] and [GROUP] to fit your needs)
6. your@machine:...nextcloud-docker-development$ `cd sensorlogger`
7. your@machine:...nextcloud-docker-development$ `git checkout 0.1-nc-devel`
8. open browser goto http://localhost:8081/ and login (user and password `admin`)

### Usage

#### Get docker containers up and running
your@machine:...nextcloud-docker-development$ `composer docker-up`

#### Stop docker containers
your@machine:...nextcloud-docker-development$ `composer docker-stop`

#### Start docker containers
your@machine:...nextcloud-docker-development$ `composer docker-start`

#### Wipe out docker containers
your@machine:...nextcloud-docker-development$ `composer docker-wipeout`

your@machine:...nextcloud-docker-development$ `sudo rm -Rf data/ html/`

### Developer notes
* xdebug installed and enabled by default
* Set **CLI Interpreter is required**
![PHPStorm CLI Interpreter settings](https://www.html5live.at/wp-content/uploads/2024/01/phpstorm-cli-interpreter-settings.png)
* Set **Path mapping is required**
* ![PHPStorm Path mappings](https://www.html5live.at/wp-content/uploads/2024/01/phpstorm-path-mappings.png)
