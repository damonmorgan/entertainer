Entertainer (The Entertainment Container)
=========

Installation
------------

* Configure .env with your local parameters.
```shell
cat <<EOT >> /Users/$USER/entertainer/.env
CONTAINERS_CONFIG_PATH=/Users/$USER/entertainer
TV_DESTINATION_PATH=/media/storage/entertainment/
PROCESSING_PATH=/Users/$USER/entertainer
PGID=$(id -g $USER)
PUID=$UID
TZ="Europe/London"
EOT
```

* Launch
```
cd /Users/$USER/entertainer/
docker-compose up -d
```
