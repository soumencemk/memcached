# Memcached My Notes !!

### Install in Docker -

```shell script
docker pull memcached
docker run --name my-memcache -d memcached
```

### Install in Ubuntu WSL
```
sudo apt-get update  
sudo apt install memcached  
```

```
ezsouka   1946  1704  0 15:55 pts/1    00:00:00 memcached
```

### Interacting with it 
```
[root@myUbuntu soumen]# telnet localhost 11211
Trying ::1...
Connected to localhost.
Escape character is '^]'.
stats items
STAT items:2:number 2
STAT items:2:age 456320
STAT items:2:evicted 0
STAT items:2:evicted_nonzero 0
STAT items:2:evicted_time 0
STAT items:2:outofmemory 0
STAT items:2:tailrepairs 0
STAT items:2:reclaimed 0

```

### Dumping the values 
```
[root@myUbuntu soumen]# memcached-tool localhost:11211 dump
Dumping memcache contents
  Number of buckets: 3
  Number of items  : 7

  xxxxxxxxxxxxxxxxxx
  xxxxxxxxxxxxxxxxxx

```