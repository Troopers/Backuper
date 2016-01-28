backuper
========

A Symfony project created on November 5, 2015, 10:30 am.

Deploy it on the server hosting the mysql database you want to backup.

Then, add this kind of crontab job:

```
0 0 * * * env SYMFONY__BACKUP__DIRECTORY="[path to backup directory]" SYMFONY__DATABASE_NAME="[database name]" SYMFONY__DATABASE_USER="[database user]" SYMFONY__DATABASE_PASSWORD="[database password]"  php [path to sources]/app/console dizda:backup:start
```
