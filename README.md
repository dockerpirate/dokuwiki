# DokuWiki


## Usage

### Create 4 volumes for backups

```shell
docker volume create dokuwiki-data 
docker volume create dokuwiki-conf 
docker volume create dokuwiki-tpl 
docker volume create dokuwiki-plugins 

docker run \
    --publish 8100:8080 \
    --name dokuwiki \
    --restart unless-stopped \
    --detach \
    -m 128m \
    dockerpirate/dokuwiki
```
