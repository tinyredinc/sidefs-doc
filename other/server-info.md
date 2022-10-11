* QC - QCloud 腾讯云
* GC - Google Cloud 谷歌云
* 服务器编码方式 - [供应商][地区][编码] - [功能备注]

QCHK122-PROXY
```
LOCATION: QC CN HK
SPECS: 1C/2G
USAGE: HK PROXY/TUNNEL FOR CN DEVS
IP1: 101.32.185.122
IP2: 172.19.19.15
OS: Ubuntu 22.04 LTS
```

GCUS051-API
```
LOCATION: GC US CENTRAL
SPECS: 2C/4G
USAGE: BACKEND SERVER FOR API(s)
IP1: 104.197.121.190
IP2: 10.10.10.51
OS: Ubuntu 22.04 LTS
ENV: Apache2.4, Php8.1
```

GCUS066-DB
```
LOCATION: GC US CENTRAL
SPECS: 4C/8G
USAGE: MYSQL PRIMARY DATABASE
IP1: 35.193.249.220
IP2: 10.165.48.3
MEMO: access ONLY FROM local network
```

GCUSXXX-WEB
```
SPECS: 2C/4G
USAGE: FRONTEND SERVER FOR WEB(s)
```

GCUSXXX-CACHE
```
SPECS: 1C/4G
USAGE: REDIS CACHE DATABASE
```


# PING TEST

```
[RED LOCAL] >> [GC CA EAST]
PING 34.130.196.158 (34.130.196.158) 56(84) bytes of data.
64 bytes from 34.130.196.158: icmp_seq=1 ttl=58 time=14.6 ms
64 bytes from 34.130.196.158: icmp_seq=2 ttl=58 time=16.2 ms
64 bytes from 34.130.196.158: icmp_seq=3 ttl=58 time=17.8 ms
64 bytes from 34.130.196.158: icmp_seq=4 ttl=58 time=16.3 ms

[RED LOCAL] >> [GC US EAST]
PING 35.243.220.82 (35.243.220.82) 56(84) bytes of data.
64 bytes from 35.243.220.82: icmp_seq=1 ttl=57 time=48.3 ms
64 bytes from 35.243.220.82: icmp_seq=2 ttl=57 time=48.7 ms
64 bytes from 35.243.220.82: icmp_seq=3 ttl=57 time=48.1 ms
64 bytes from 35.243.220.82: icmp_seq=4 ttl=57 time=46.3 ms

[RED LOCAL] >> [GC US CENTRAL]
PING 104.197.121.190 (104.197.121.190) 56(84) bytes of data.
64 bytes from 104.197.121.190: icmp_seq=1 ttl=58 time=48.1 ms
64 bytes from 104.197.121.190: icmp_seq=2 ttl=58 time=52.4 ms
64 bytes from 104.197.121.190: icmp_seq=3 ttl=58 time=48.7 ms
64 bytes from 104.197.121.190: icmp_seq=4 ttl=58 time=49.7 ms

[RED LOCAL] >> [GC US WEST]
PING 34.168.167.162 (34.168.167.162) 56(84) bytes of data.
64 bytes from 34.168.167.162: icmp_seq=1 ttl=58 time=81.2 ms
64 bytes from 34.168.167.162: icmp_seq=2 ttl=58 time=80.3 ms
64 bytes from 34.168.167.162: icmp_seq=3 ttl=58 time=82.8 ms
64 bytes from 34.168.167.162: icmp_seq=4 ttl=58 time=87.1 ms
```

```


[GC CA EAST] >> [GC CN HK]
PING 35.215.191.195 (35.215.191.195) 56(84) bytes of data.
64 bytes from 35.215.191.195: icmp_seq=1 ttl=61 time=217 ms
64 bytes from 35.215.191.195: icmp_seq=2 ttl=61 time=216 ms
64 bytes from 35.215.191.195: icmp_seq=3 ttl=61 time=216 ms
64 bytes from 35.215.191.195: icmp_seq=4 ttl=61 time=216 ms

[GC US EAST] >> [GC CN HK]
PING 35.215.191.195 (35.215.191.195) 56(84) bytes of data.
64 bytes from 35.215.191.195: icmp_seq=1 ttl=50 time=190 ms
64 bytes from 35.215.191.195: icmp_seq=2 ttl=50 time=189 ms
64 bytes from 35.215.191.195: icmp_seq=3 ttl=50 time=189 ms
64 bytes from 35.215.191.195: icmp_seq=4 ttl=50 time=189 ms

[GC US CENTAL] >> [GC CN HK]
PING 35.215.191.195 (35.215.191.195) 56(84) bytes of data.
64 bytes from 35.215.191.195: icmp_seq=1 ttl=50 time=192 ms
64 bytes from 35.215.191.195: icmp_seq=2 ttl=50 time=190 ms
64 bytes from 35.215.191.195: icmp_seq=3 ttl=50 time=190 ms
64 bytes from 35.215.191.195: icmp_seq=4 ttl=50 time=190 ms

[GC US CENTAL] >> [QC CN HK]
PING 101.32.185.122 (101.32.185.122) 56(84) bytes of data.
64 bytes from 101.32.185.122: icmp_seq=1 ttl=59 time=191 ms
64 bytes from 101.32.185.122: icmp_seq=2 ttl=59 time=190 ms
64 bytes from 101.32.185.122: icmp_seq=3 ttl=59 time=189 ms
64 bytes from 101.32.185.122: icmp_seq=4 ttl=59 time=190 ms

[GC US WEST] >> [GC CN HK]
PING 35.215.191.195 (35.215.191.195) 56(84) bytes of data.
64 bytes from 35.215.191.195: icmp_seq=1 ttl=60 time=138 ms
64 bytes from 35.215.191.195: icmp_seq=2 ttl=60 time=135 ms
64 bytes from 35.215.191.195: icmp_seq=3 ttl=60 time=135 ms
64 bytes from 35.215.191.195: icmp_seq=4 ttl=60 time=135 ms
```