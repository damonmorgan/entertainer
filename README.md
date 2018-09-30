Entertainer (The Entertainment Container)
=========

Installation
------------

* Configure .env with your local parameters.
```shell
cat <<EOT >> /home/$USER/entertainer/.env
CONTAINERS_CONFIG_PATH=/home/$USER/entertainer
TV_DESTINATION_PATH=/media/storage/entertainment/tv
PROCESSING_PATH=/home/$USER/entertainer
PGID=$(id -g $USER)
PUID=$UID
TZ="Europe/London"
EOT
```

* Launch
```
cd /home/$USER/entertainer/
docker-compose up -d
```

TODO
------------

* There is an issue with docker compose interpolating integers so `PUID` and `PGID` end up as strings so for now they are hardcoded as the default ubuntu user id in the compose file.
