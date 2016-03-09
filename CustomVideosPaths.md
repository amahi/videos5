If you store your videos somewhere else than the default /var/hda/files/movies, you'll need to change that path in the Videos5 settings. Execute those two commands, from a terminal:

```
mysql -uvideos5 -pvideos5 -e "update settings set value='/path/to/your/videos' where name = 'paths'" videos5
```
```
/usr/bin/php /var/hda/web-apps/videos5/html/index.php find
```

If you want to scan multiple directories, separate each by \n in the above mysql command:
```
mysql -uvideos5 -pvideos5 -e "update settings set value='/path/to/your/videos\n/other_path/to/your/other_videos' where name = 'paths'" videos5
```