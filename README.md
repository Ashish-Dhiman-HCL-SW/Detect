me "root".
Pre-authentication banner message from server:
| This system is restricted to authorized users. Individuals attempting unautho
> rized access will be prosecuted. If unauthorized, terminate access now! Click
> ing on OK indicates your acceptance of the information in the background.
|
End of banner message from server
This system is restricted to authorized users. Individuals attempting unauthorized access will be prosecuted. If unauthorized, terminate access now! Clicking on OK indicates your acceptance of the information in the background.

Activate the web console with: systemctl enable --now cockpit.socket

Register this system with Red Hat Insights: insights-client --register
Create an account or view all your systems at https://red.ht/insights-dashboard
Last login: Mon Feb 16 16:35:50 2026 from 10.1.254.5
[root@hcl-gb-qu-ced-3002 ~]# ls
 anaconda-ks.cfg   cmake-filesystem-3.26.5-2.el8.x86_64.rpm   Documents   initial-setup-ks.cfg   librdkafka1-2.4.0-2.cflt.el8.x86_64.rpm   node_exporter  'Snow Agent -Linux'                       tmxbc
 checksum          config.json                                download    kafka_2.13-3.7.0       manifest                                  Pictures        Templates                                Videos
 checksum.p7       Desktop                                    Downloads   kafka_2.13-3.7.0.tgz   Music                                     Public          TMSensorAgent_Linux_auto_x86_64_V4.tar
[root@hcl-gb-qu-ced-3002 ~]# df -h
Filesystem             Size  Used Avail Use% Mounted on
devtmpfs               7.7G     0  7.7G   0% /dev
tmpfs                  7.7G   92K  7.7G   1% /dev/shm
tmpfs                  7.7G   18M  7.7G   1% /run
tmpfs                  7.7G     0  7.7G   0% /sys/fs/cgroup
/dev/mapper/rhel-root   47G   42G  4.9G  90% /
/dev/mapper/vg01-lv01  200G  1.7G  199G   1% /data
/dev/sda2             1014M  415M  600M  41% /boot
/dev/sda1              599M  5.9M  593M   1% /boot/efi
tmpfs                  1.6G  8.0K  1.6G   1% /run/user/42
tmpfs                  1.6G     0  1.6G   0% /run/user/0
overlay                 47G   42G  4.9G  90% /var/lib/containers/storage/overlay/metacopy-check1720684787/merged
[root@hcl-gb-qu-ced-3002 ~]# cd /home/
[root@hcl-gb-qu-ced-3002 home]# ls
addmitam  ansible  driveadmin  inframgr  mysql  rscd  SOCVA  splunk  user
[root@hcl-gb-qu-ced-3002 home]# ls -ltra
total 8
drwx------. 15       1000       1000 4096 Oct 30  2023 user
drwxr-x---   2 root       root         31 Apr 24  2024 rscd
drwx------   3 mysql      mysql        78 Dec  9  2024 mysql
dr-xr-xr-x. 18 root       root        256 Jan 23  2025 ..
drwx------   5 addmitam   addmitam    145 Mar 30  2025 addmitam
drwx------   3 splunk     splunk       78 Aug 19 12:38 splunk
drwxr-xr-x. 11 root       root        135 Nov 15 12:31 .
drwx------   6 ansible    ansible     138 Dec  9 12:03 ansible
drwx------   4 inframgr   inframgr    123 Jan 23 18:14 inframgr
drwxr-x---  11 driveadmin driveadmin 4096 Feb 11 16:05 driveadmin
drwx------   6 SOCVA      SOCVA       170 Feb 13 03:26 SOCVA
[root@hcl-gb-qu-ced-3002 home]# cd driveadmin/
[root@hcl-gb-qu-ced-3002 driveadmin]# ls
12.1.8_Backup  acme  acme.tar  custom_event_consumer  drive  external  HCL_Detect_12.1.9_rhel08.tar.gz  HCLDetectv12.1.9-LICENSE.txt  HCLDetectv12.1.9-NOTICE.txt  instance_home  instance_home.tar
[root@hcl-gb-qu-ced-3002 driveadmin]# cd custom_event_consumer/
[root@hcl-gb-qu-ced-3002 custom_event_consumer]# ls
Makefile  pom-custom.xml  README  src
[root@hcl-gb-qu-ced-3002 custom_event_consumer]# cd ..
[root@hcl-gb-qu-ced-3002 driveadmin]# ld
ld: no input files
[root@hcl-gb-qu-ced-3002 driveadmin]# ls
12.1.8_Backup  acme  acme.tar  custom_event_consumer  drive  external  HCL_Detect_12.1.9_rhel08.tar.gz  HCLDetectv12.1.9-LICENSE.txt  HCLDetectv12.1.9-NOTICE.txt  instance_home  instance_home.tar
[root@hcl-gb-qu-ced-3002 driveadmin]#
[root@hcl-gb-qu-ced-3002 driveadmin]# pwd
/home/driveadmin
[root@hcl-gb-qu-ced-3002 driveadmin]# du -sch *
5.3G    12.1.8_Backup
4.1M    acme
3.9M    acme.tar
44K     custom_event_consumer
763M    drive
3.1G    external
1.3G    HCL_Detect_12.1.9_rhel08.tar.gz
4.0K    HCLDetectv12.1.9-LICENSE.txt
552K    HCLDetectv12.1.9-NOTICE.txt
14G     instance_home
661M    instance_home.tar
25G     total
[root@hcl-gb-qu-ced-3002 driveadmin]# cd instance_home/
[root@hcl-gb-qu-ced-3002 instance_home]# du -sch *
3.5M    applications
0       data
608M    fastpast
216K    fastpast_backup_1208
0       java
8.0K    jupyter
13G     kafka
76M     kafka_backup_1208
524K    name_service
662M    pinpoint
2.1M    pinpoint_backup_1208
210M    tomcat
14G     total
[root@hcl-gb-qu-ced-3002 instance_home]# cd kafka
[root@hcl-gb-qu-ced-3002 kafka]# du -sch *
13G     kafka_data
0       kafka_logs
4.0K    kafka.pid
4.0K    kafka.stderr
0       kafka.stdout
8.0K    log4j.properties
8.0K    server.properties
664K    zookeeper_data
4.0K    zookeeper.pid
4.0K    zookeeper.properties
4.0K    zookeeper.stderr
0       zookeeper.stdout
13G     total
[root@hcl-gb-qu-ced-3002 kafka]# cd kafka_data/
[root@hcl-gb-qu-ced-3002 kafka_data]# ls
APPLICATION-CUSTOMER_PROFILE_REFRESH-0  APPLICATION-UPI_P2P_DEBIT-1  __consumer_offsets-15  __consumer_offsets-23  __consumer_offsets-31  __consumer_offsets-4   __consumer_offsets-48                     log-start-offset-checkpoint
APPLICATION-CUSTOMER_PROFILE_REFRESH-1  cleaner-offset-checkpoint    __consumer_offsets-16  __consumer_offsets-24  __consumer_offsets-32  __consumer_offsets-40  __consumer_offsets-49                     meta.properties
APPLICATION-ERICSSON_USAGE-0            __consumer_offsets-0         __consumer_offsets-17  __consumer_offsets-25  __consumer_offsets-33  __consumer_offsets-41  __consumer_offsets-5                      recovery-point-offset-checkpoint
APPLICATION-ERICSSON_USAGE-1            __consumer_offsets-1         __consumer_offsets-18  __consumer_offsets-26  __consumer_offsets-34  __consumer_offsets-42  __consumer_offsets-6                      replication-offset-checkpoint
APPLICATION-RECHARGE-0                  __consumer_offsets-10        __consumer_offsets-19  __consumer_offsets-27  __consumer_offsets-35  __consumer_offsets-43  __consumer_offsets-7                      SYSTEM-RESPONSE_MESSAGES-0
APPLICATION-RECHARGE-1                  __consumer_offsets-11        __consumer_offsets-2   __consumer_offsets-28  __consumer_offsets-36  __consumer_offsets-44  __consumer_offsets-8                      SYSTEM-RESPONSE_MESSAGES-1
APPLICATION-TOPUP_DEMO-0                __consumer_offsets-12        __consumer_offsets-20  __consumer_offsets-29  __consumer_offsets-37  __consumer_offsets-45  __consumer_offsets-9
APPLICATION-TOPUP_DEMO-1                __consumer_offsets-13        __consumer_offsets-21  __consumer_offsets-3   __consumer_offsets-38  __consumer_offsets-46  INTERNAL_EVENT_COMMUNICATION_TOPIC-0
APPLICATION-UPI_P2P_DEBIT-0             __consumer_offsets-14        __consumer_offsets-22  __consumer_offsets-30  __consumer_offsets-39  __consumer_offsets-47  INTERNAL_PROCESS_ACTUATION_KAFKA_TOPIC-0
[root@hcl-gb-qu-ced-3002 kafka_data]# du -sch *
8.0K    APPLICATION-CUSTOMER_PROFILE_REFRESH-0
8.0K    APPLICATION-CUSTOMER_PROFILE_REFRESH-1
8.0K    APPLICATION-ERICSSON_USAGE-0
8.0K    APPLICATION-ERICSSON_USAGE-1
8.0K    APPLICATION-RECHARGE-0
8.0K    APPLICATION-RECHARGE-1
8.0K    APPLICATION-TOPUP_DEMO-0
8.0K    APPLICATION-TOPUP_DEMO-1
2.3G    APPLICATION-UPI_P2P_DEBIT-0
2.3G    APPLICATION-UPI_P2P_DEBIT-1
4.0K    cleaner-offset-checkpoint
8.0K    __consumer_offsets-0
8.0K    __consumer_offsets-1
2.9M    __consumer_offsets-10
8.0K    __consumer_offsets-11
8.0K    __consumer_offsets-12
38M     __consumer_offsets-13
648K    __consumer_offsets-14
8.0K    __consumer_offsets-15
8.0K    __consumer_offsets-16
8.0K    __consumer_offsets-17
8.0K    __consumer_offsets-18
8.0K    __consumer_offsets-19
8.0K    __consumer_offsets-2
8.0K    __consumer_offsets-20
8.0K    __consumer_offsets-21
8.0K    __consumer_offsets-22
8.0K    __consumer_offsets-23
8.0K    __consumer_offsets-24
8.0K    __consumer_offsets-25
8.0K    __consumer_offsets-26
36K     __consumer_offsets-27
8.0K    __consumer_offsets-28
8.0K    __consumer_offsets-29
8.0K    __consumer_offsets-3
8.0K    __consumer_offsets-30
8.0K    __consumer_offsets-31
8.0K    __consumer_offsets-32
8.0K    __consumer_offsets-33
8.0K    __consumer_offsets-34
8.0K    __consumer_offsets-35
8.0K    __consumer_offsets-36
8.0K    __consumer_offsets-37
36K     __consumer_offsets-38
8.0K    __consumer_offsets-39
40K     __consumer_offsets-4
8.0K    __consumer_offsets-40
8.0K    __consumer_offsets-41
8.0K    __consumer_offsets-42
8.0K    __consumer_offsets-43
8.0K    __consumer_offsets-44
38M     __consumer_offsets-45
8.0K    __consumer_offsets-46
8.0K    __consumer_offsets-47
8.0K    __consumer_offsets-48
8.0K    __consumer_offsets-49
40K     __consumer_offsets-5
8.0K    __consumer_offsets-6
8.0K    __consumer_offsets-7
40K     __consumer_offsets-8
8.0K    __consumer_offsets-9
3.6G    INTERNAL_EVENT_COMMUNICATION_TOPIC-0
3.4G    INTERNAL_PROCESS_ACTUATION_KAFKA_TOPIC-0
4.0K    log-start-offset-checkpoint
4.0K    meta.properties
4.0K    recovery-point-offset-checkpoint
4.0K    replication-offset-checkpoint
310M    SYSTEM-RESPONSE_MESSAGES-0
310M    SYSTEM-RESPONSE_MESSAGES-1
13G     total
[root@hcl-gb-qu-ced-3002 kafka_data]# ls -ltra
total 92
-rw-r-----  1 driveadmin driveadmin   88 Jan 16 17:09 meta.properties
drwxr-x---  5 driveadmin driveadmin 4096 Feb  3 19:09 ..
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-0
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-48
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-29
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-26
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-7
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-42
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-TOPUP_DEMO-1
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-23
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-1
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-39
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-20
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-17
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-36
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-RECHARGE-0
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-33
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-49
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-11
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-30
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-46
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-24
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-43
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-ERICSSON_USAGE-0
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-CUSTOMER_PROFILE_REFRESH-0
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-21
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-2
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-40
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-37
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-18
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-RECHARGE-1
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-34
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-15
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-CUSTOMER_PROFILE_REFRESH-1
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-12
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-31
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-9
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-47
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-19
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-28
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-35
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-44
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-6
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-25
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-16
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-22
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-41
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-ERICSSON_USAGE-1
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 APPLICATION-TOPUP_DEMO-0
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-32
drwxr-x---  2 driveadmin driveadmin  167 Feb  3 19:09 __consumer_offsets-3
-rw-r-----  1 driveadmin driveadmin  233 Feb 13 13:06 cleaner-offset-checkpoint
-rw-r-----  1 driveadmin driveadmin 1703 Feb 14 10:33 replication-offset-checkpoint
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 SYSTEM-RESPONSE_MESSAGES-0
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-27
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-45
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-10
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-4
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-38
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-14
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 INTERNAL_EVENT_COMMUNICATION_TOPIC-0
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-13
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-8
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 SYSTEM-RESPONSE_MESSAGES-1
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 INTERNAL_PROCESS_ACTUATION_KAFKA_TOPIC-0
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 APPLICATION-UPI_P2P_DEBIT-0
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 APPLICATION-UPI_P2P_DEBIT-1
drwxr-x---  2 driveadmin driveadmin 4096 Feb 14 10:33 __consumer_offsets-5
-rw-r-----  1 driveadmin driveadmin 1703 Feb 14 10:33 recovery-point-offset-checkpoint
-rw-r-----  1 driveadmin driveadmin    4 Feb 14 10:33 log-start-offset-checkpoint
-rw-r-----  1 driveadmin driveadmin   30 Feb 14 10:33 .kafka_cleanshutdown
drwxr-x--- 66 driveadmin driveadmin 4096 Feb 14 10:33 .
[root@hcl-gb-qu-ced-3002 kafka_data]# du -sch * | grep G
8.0K    APPLICATION-ERICSSON_USAGE-0
8.0K    APPLICATION-ERICSSON_USAGE-1
8.0K    APPLICATION-RECHARGE-0
8.0K    APPLICATION-RECHARGE-1
2.3G    APPLICATION-UPI_P2P_DEBIT-0
2.3G    APPLICATION-UPI_P2P_DEBIT-1
3.6G    INTERNAL_EVENT_COMMUNICATION_TOPIC-0
3.4G    INTERNAL_PROCESS_ACTUATION_KAFKA_TOPIC-0
310M    SYSTEM-RESPONSE_MESSAGES-0
310M    SYSTEM-RESPONSE_MESSAGES-1
13G     total
[root@hcl-gb-qu-ced-3002 kafka_data]# df -h
Filesystem             Size  Used Avail Use% Mounted on
devtmpfs               7.7G     0  7.7G   0% /dev
tmpfs                  7.7G   92K  7.7G   1% /dev/shm
tmpfs                  7.7G   18M  7.7G   1% /run
tmpfs                  7.7G     0  7.7G   0% /sys/fs/cgroup
/dev/mapper/rhel-root   47G   42G  4.9G  90% /
/dev/mapper/vg01-lv01  200G  1.7G  199G   1% /data
/dev/sda2             1014M  415M  600M  41% /boot
/dev/sda1              599M  5.9M  593M   1% /boot/efi
tmpfs                  1.6G  8.0K  1.6G   1% /run/user/42
tmpfs                  1.6G     0  1.6G   0% /run/user/0
overlay                 47G   42G  4.9G  90% /var/lib/containers/storage/overlay/metacopy-check1720684787/merged
