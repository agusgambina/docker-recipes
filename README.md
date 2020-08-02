## Linux

### Folder structure

```
$ mkdir -p /home/$USER/storage/PlexMediaServer/config
$ mkdir -p /home/$USER/storage/media/video
$ mkdir -p /home/$USER/storage/media/music
$ mkdir -p /home/$USER/storage/downloads/p2p/torrents/config
$ mkdir -p /home/$USER/storage/downloads/p2p/torrents/incoming
$ mkdir -p /home/$USER/storage/downloads/p2p/torrents/watch
```

### Environment variables

Add these environment variables to `~/.bashrc` or `~/.zshrc`

```
export PLEX_CLAIM="claim-PLEX_CLAIM"
```

### Run

```
$ docker-compose up -d
```

### External Hard Drive

#### Permanently mount external hard-drive

0. Install requirements

```
$ sudo apt-get update -y
$ sudo apt-get install -y fuse
$ sudo apt-get install -y exfat-fuse
$ sudo apt-get install -y exfat-utils
```

1. Make a folder, called, for example /media/driveone

```
$ sudo mkdir /media/driveone
```

2. Make yourself the owner of this folder:

```
$ sudo chown -R $(id -u):$(id -u) /media/driveone
```

3. Get UUID from hard drive

```
$ sudo blkid
```

4. Add a line to your `/etc/fstab` like the following:

```
UUID=5DFA-D489 /media/driveone exfat defaults,nofail 0       1
```