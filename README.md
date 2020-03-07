Entertainer (The Entertainment Container)
=========

Installation
------------

Run all the following from inside the entertainer dir
```shell
cd ~/entertainer/
```

* Configure .env with your local parameters.
```
cat <<EOT >> .env
CONTAINERS_CONFIG_PATH=$(pwd)
TV_DESTINATION_PATH=/media/storage/entertainment/tv
MOVIE_DESTINATION_PATH=/media/storage/entertainment/movies
PROCESSING_PATH=$(pwd)
BACKUP_PATH=/media/storage
PGID=$(id -g $USER)
PUID=$UID
TZ="Europe/London"
EOT
```

* My .env
```
cat <<EOT >> .env
CONTAINERS_CONFIG_PATH=/media/wdred-alpha/entertainer-config
TV_DESTINATION_PATH=/media/wdred-bravo/Entertainment/TV
MOVIE_DESTINATION_PATH=/media/wdred-charlie/Entertainment/HD-Movies-Downloaded
PROCESSING_PATH=/home/damon/entertainer
BACKUP_PATH=/media
PGID=1000
PUID=1000
TZ="Europe/London"
EOT
```

* Launch
```shell
docker-compose up -d
```

Updating
------------

```shell
./update
```

TODO
------------

* There is an issue with docker compose interpolating integers so `PUID` and `PGID` end up as strings so for now they are hardcoded as the default ubuntu user id in the compose file.
