# DokuWiki

docker run \
    --publish 8100:8080 \
    --name dokuwiki \
    --restart unless-stopped \
    --detach \
    -m 128m \
    dockerpirate/dokuwiki
    
create 4 volumes for backups
 # data , conf, tpl, plugins
