<!--
N.B.: This README was automatically generated by <https://github.com/YunoHost/apps/tree/master/tools/readme_generator>
It shall NOT be edited by hand.
-->

# PeerTube for YunoHost

[![Integration level](https://dash.yunohost.org/integration/peertube.svg)](https://ci-apps.yunohost.org/ci/apps/peertube/) ![Working status](https://ci-apps.yunohost.org/ci/badges/peertube.status.svg) ![Maintenance status](https://ci-apps.yunohost.org/ci/badges/peertube.maintain.svg)

[![Install PeerTube with YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=peertube)

*[Read this README in other languages.](./ALL_README.md)*

> *This package allows you to install PeerTube quickly and simply on a YunoHost server.*  
> *If you don't have YunoHost, please consult [the guide](https://yunohost.org/install) to learn how to install it.*

## Overview

PeerTube is a decentralized and federated video hosting software. To publish videos, the user must register with a host (called an instance). Each host has its own conditions of use (storage space per user, moderation rules, themes, etc.). Thanks to WebTorrent, if several people view the same video, fragments of it are exchanged between people so as not to overload the instance. Decentralized: Each instance can follow one or more other PeerTube instances in order to allow its users to view their videos. Federated: Via the ActivityPub protocol, Peertube can interact with other software that is part of the Fediverse, such as Mastodon for example.


**Shipped version:** 6.3.0~ynh1

**Demo:** <http://peertube.cpy.re>

## Screenshots

![Screenshot of PeerTube](./doc/screenshots/screenshot1.jpg)

## Documentation and resources

- Official app website: <https://joinpeertube.org/fr>
- Official admin documentation: <https://docs.joinpeertube.org>
- Upstream app code repository: <https://github.com/Chocobozzz/PeerTube>
- YunoHost Store: <https://apps.yunohost.org/app/peertube>
- Report a bug: <https://github.com/YunoHost-Apps/peertube_ynh/issues>

## Developer info

Please send your pull request to the [`testing` branch](https://github.com/YunoHost-Apps/peertube_ynh/tree/testing).

To try the `testing` branch, please proceed like that:

```bash
sudo yunohost app install https://github.com/YunoHost-Apps/peertube_ynh/tree/testing --debug
or
sudo yunohost app upgrade peertube -u https://github.com/YunoHost-Apps/peertube_ynh/tree/testing --debug
```

**More info regarding app packaging:** <https://yunohost.org/packaging_apps>
