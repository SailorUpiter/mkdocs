```
[fiotest]
rw=randwrite
name=fiotest
blocksize=4k
filename=/mnt/pve/test/write
size=100g
ioengine=libaio
iodepth=1
numjobs=1
runtime=60
direct=1
```
