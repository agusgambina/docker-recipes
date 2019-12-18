## Linux

### Folder structure

```
$ mkdir -p /home/$USER/storage/PlexMediaServer/config
$ mkdir -p /home/$USER/storage/media/video
$ mkdir -p /home/$USER/storage/media/music
$ mkdir -p /home/$USER/storage/downloads/p2p/torrents/config
$ mkdir -p /home/$USER/storage/downloads/p2p/torrents/incoming
$ mkdir -p /home/$USER/storage/downloads/p2p/torrents/watch
$ mkdir -p /home/$USER/storage/downloads/p2p/amule/conf
$ mkdir -p /home/$USER/storage/downloads/p2p/amule/temp
$ mkdir -p /home/$USER/storage/downloads/p2p/amule/incoming
```

### Environment variables

Add these environment variables to `~/.bashrc` or `~/.zshrc`

```
export PLEX_CLAIM="claim-PLEX_CLAIM"
export SAMBA_USER="SAMBA_USER"
export SAMBA_PASSWORD="SAMBA_PASSWORD"
```

### Run

```
$ docker-compose up -d
```