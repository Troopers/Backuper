# Backuper

Run on the server hosting the mysql database you want to backup.

Then, add this kind of crontab job:

```
0 0 * * * env SYMFONY__BACKUP__DIRECTORY="[path to backup directory]" SYMFONY__DATABASE_NAME="[database name]" SYMFONY__DATABASE_USER="[database user]" SYMFONY__DATABASE_PASSWORD="[database password]"  php [path to sources]/app/console dizda:backup:start --env=dev
```
`keep the dev environment argument to be sure your env variables will override parameters`

## Requirements

You need to have the ssh2 extension and 7z.

### Ubuntu / Debian
```
sudo apt-get install php5-ssh2 p7zip-full
or
sudo apt-get install php7.0-ssh2 p7zip-full
```
