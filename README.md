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

### First Setup

You can now visit the install page to configure your new DokuWiki wiki.

For example, if you are running container locally, you can acces the page in browser by going to http://localhost/install.php

After that remove install.php from /srv it.

### Troubleshooting

If upgrading from v2018, you have to remove old conf and plugins folders

### License

[The MIT License](LICENSE)
