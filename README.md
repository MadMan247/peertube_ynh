# ovh_fix branch for peertube_ynh

If installing on an ovh virtual machine or having `gyp ERR! configure error` please follow the steps below

## Steps for installing

1. Install nodejs

```
$ curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```

2. Install the peertube with **OVH fix** branch.

```
$ yunohost app install https://github.com/YunoHost-Apps/peertube_ynh/tree/ovh_fix --debug
```

3. After installation is complete run **yarn install**.

```
$ cd /var/www/peertube && yarn install --production --pure-lockfile
```

4. Give proper **permissions** to peertube

```
$ chown -R peertube:peertube /var/www/peertube
```

5. **Restart peertube** and check if there is any error message.

```
$ service peertube restart
$ journalctl -feu peertube
```

6. If there is no **error in red** in the last lines of log. Press **ctrl+c** to stop the logs.

7. Go to your **domain** to check if peertube is running and everthing is ok.

8. Change your **root password** by this command:

```
    $ cd /var/www/peertube && NODE_CONFIG_DIR="/var/www/peertube/config/" NODE_ENV=production npm run reset-password -- -u root
```

Username: **root**
password: **created in above step**

## Steps for upgrading

1. Upgrade peertube  with **OVH fix** branch.

```
$ yunohost app upgrade peertube -u https://github.com/YunoHost-Apps/peertube_ynh/tree/ovh_fix --debug
```

2. After upgrade is complete run **yarn install**.

```
$ cd /var/www/peertube && sudo yarn install --production --pure-lockfile
```

3. Give proper **permissions** to peertube

```
$ chown -R peertube:peertube /var/www/peertube
```

4. **Restart peertube** and check if there is any error message.

```
$ service peertube restart
```

**More info regarding app packaging:** https://yunohost.org/packaging_apps