# hive-in-powersheel

FIRST START NAME NODE

Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Install the latest PowerShell for new features and improvements! https://aka.ms/PSWindows

PS C:\Users\souvi> docker exec -it namenode bash
root@d580499e8090:/# hadoop fs -ls  /
Found 5 items
drwxr-xr-x   - root supergroup          0 2023-02-16 06:51 /data
drwxr-xr-x   - root supergroup          0 2023-02-15 18:46 /data_files
drwxr-xr-x   - root supergroup          0 2023-02-15 07:58 /rmstate
drwxrwxr-x   - root supergroup          0 2023-02-15 07:59 /tmp
drwxr-xr-x   - root supergroup          0 2023-02-15 07:59 /user
root@d580499e8090:/# hadoop fs -ls  /data
Found 1 items
drwxr-xr-x   - root supergroup          0 2023-02-16 06:51 /data/openbeer
root@d580499e8090:/# hadoop fs -ls  /data_files
root@d580499e8090:/# ls /
KEYS  boot           dev            etc     hadoop-data  lib    media  opt   root  run.sh  srv  tmp  var
bin   breweries.csv  entrypoint.sh  hadoop  home         lib64  mnt    proc  run   sbin    sys  usr
root@d580499e8090:/# ls -ltr
total 440
drwxr-xr-x   2 root root   4096 Sep  8  2019 home
drwxr-xr-x   2 root root   4096 Sep  8  2019 boot
drwxr-xr-x   1 root root   4096 Jan 30  2020 var
drwxr-xr-x   1 root root   4096 Jan 30  2020 usr
drwxr-xr-x   2 root root   4096 Jan 30  2020 srv
drwxr-xr-x   3 root root   4096 Jan 30  2020 run
drwxr-xr-x   2 root root   4096 Jan 30  2020 mnt
drwxr-xr-x   2 root root   4096 Jan 30  2020 media
drwxr-xr-x   2 root root   4096 Jan 30  2020 lib64
drwxr-xr-x   1 root root   4096 Jan 30  2020 lib
-rwxr-xr-x   1 root root   4155 Feb  4  2020 entrypoint.sh
drwxr-xr-x   1 root root   4096 Feb  4  2020 sbin
drwxr-xr-x   1 root root   4096 Feb  4  2020 bin
-rw-r--r--   1 root root 325083 Feb  4  2020 KEYS
drwxr-xr-x   1 root root   4096 Feb  4  2020 opt
drwxr-xr-x   2 root root   4096 Feb  4  2020 hadoop-data
-rwxr-xr-x   1 root root    494 Feb  4  2020 run.sh
drwxr-xr-x   3 root root   4096 Feb  4  2020 hadoop
-rwxr-xr-x   1 root root  25188 Feb 12 18:36 breweries.csv
drwxr-xr-x   1 root root   4096 Feb 15 07:53 etc
drwx------   1 root root   4096 Feb 15 18:16 root
dr-xr-xr-x  11 root root      0 Feb 16 15:40 sys
dr-xr-xr-x 630 root root      0 Feb 16 15:40 proc
drwxr-xr-x   5 root root    340 Feb 16 15:40 dev
drwxrwxrwt   1 root root   4096 Feb 16 15:40 tmp
root@d580499e8090:/# exit
exit
PS C:\Users\souvi> docker cp G:\New_folder\depart_data.csv namenode:/
PS C:\Users\souvi> docker exec -it namenode bash
root@d580499e8090:/# ls -ltr
total 444
drwxr-xr-x   2 root root   4096 Sep  8  2019 home
drwxr-xr-x   2 root root   4096 Sep  8  2019 boot
drwxr-xr-x   1 root root   4096 Jan 30  2020 var
drwxr-xr-x   1 root root   4096 Jan 30  2020 usr
drwxr-xr-x   2 root root   4096 Jan 30  2020 srv
drwxr-xr-x   3 root root   4096 Jan 30  2020 run
drwxr-xr-x   2 root root   4096 Jan 30  2020 mnt
drwxr-xr-x   2 root root   4096 Jan 30  2020 media
drwxr-xr-x   2 root root   4096 Jan 30  2020 lib64
drwxr-xr-x   1 root root   4096 Jan 30  2020 lib
-rwxr-xr-x   1 root root   4155 Feb  4  2020 entrypoint.sh
drwxr-xr-x   1 root root   4096 Feb  4  2020 sbin
drwxr-xr-x   1 root root   4096 Feb  4  2020 bin
-rw-r--r--   1 root root 325083 Feb  4  2020 KEYS
drwxr-xr-x   1 root root   4096 Feb  4  2020 opt
drwxr-xr-x   2 root root   4096 Feb  4  2020 hadoop-data
-rwxr-xr-x   1 root root    494 Feb  4  2020 run.sh
drwxr-xr-x   3 root root   4096 Feb  4  2020 hadoop
-rwxr-xr-x   1 root root  25188 Feb 12 18:36 breweries.csv
drwxr-xr-x   1 root root   4096 Feb 15 07:53 etc
drwx------   1 root root   4096 Feb 15 18:16 root
-rwxr-xr-x   1 root root    655 Feb 16 07:14 depart_data.csv
dr-xr-xr-x  11 root root      0 Feb 16 15:40 sys
dr-xr-xr-x 904 root root      0 Feb 16 15:40 proc
drwxr-xr-x   5 root root    340 Feb 16 15:40 dev
drwxrwxrwt   1 root root   4096 Feb 16 15:40 tmp
root@d580499e8090:/# hadoop fs -put depart_data.csv /data_files
2023-02-16 15:56:21,882 INFO sasl.SaslDataTransferClient: SASL encryption trust check: localHostTrusted = false, remoteHostTrusted = false
root@d580499e8090:/# hadoop fs -ls /data_files
Found 1 items
-rw-r--r--   3 root supergroup        655 2023-02-16 15:56 /data_files/depart_data.csv
root@d580499e8090:/#
