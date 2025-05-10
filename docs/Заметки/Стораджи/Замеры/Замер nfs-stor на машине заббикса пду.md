
конфиг
[fiotest]
rw=write
name=fiotest
blocksize=8k
filename=/mnt/pve/test/write
size=1g
ioengine=libaio
iodepth=128
numjobs=1
runtime=60
direct=1

Результат
fiotest: (g=0): rw=write, bs=(R) 4096B-4096B, (W) 4096B-4096B, (T) 4096B-4096B, ioengine=libaio, iodepth=1
fio-3.28
Starting 1 process
fiotest: Laying out IO file (1 file / 1024MiB)
^Cbs: 1 (f=1): [W(1)][33.3%][w=1001KiB/s][w=250 IOPS][eta 00m:40s]
fio: terminating on signal 2

fiotest: (groupid=0, jobs=1): err= 0: pid=2515: Sat May  3 00:11:44 2025
  write: IOPS=306, BW=1227KiB/s (1257kB/s)(24.2MiB/20224msec); 0 zone resets
    slat (nsec): min=9129, max=61388, avg=11072.73, stdev=2469.71
    clat (usec): min=1575, max=237505, avg=3247.15, stdev=5187.99
     lat (usec): min=1585, max=237546, avg=3258.36, stdev=5188.33
    clat percentiles (usec):
     |  1.00th=[  1745],  5.00th=[  1909], 10.00th=[  2008], 20.00th=[  2180],
     | 30.00th=[  2311], 40.00th=[  2442], 50.00th=[  2573], 60.00th=[  2737],
     | 70.00th=[  2966], 80.00th=[  3294], 90.00th=[  4228], 95.00th=[  5866],
     | 99.00th=[ 11994], 99.50th=[ 16319], 99.90th=[ 90702], 99.95th=[103285],
     | 99.99th=[238027]
   bw (  KiB/s): min=  672, max= 1888, per=99.49%, avg=1221.60, stdev=244.70, samples=40
   iops        : min=  168, max=  472, avg=305.40, stdev=61.18, samples=40
  lat (msec)   : 2=9.88%, 4=78.65%, 10=9.69%, 20=1.50%, 50=0.10%
  lat (msec)   : 100=0.11%, 250=0.08%
  cpu          : usr=0.17%, sys=0.29%, ctx=6206, majf=0, minf=12
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,6205,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
  WRITE: bw=1227KiB/s (1257kB/s), 1227KiB/s-1227KiB/s (1257kB/s-1257kB/s), io=24.2MiB (25.4MB), run=20224-20224msec

Disk stats (read/write):
    dm-0: ios=54/8018, merge=0/0, ticks=636/27836, in_queue=28472, util=97.85%, aggrios=54/7434, aggrmerge=0/861, aggrticks=638/24232, aggrin_queue=24906, aggrutil=97.59%
  sda: ios=54/7434, merge=0/861, ticks=638/24232, in_queue=24906, util=97.59%

Конфиг
[fiotest]
rw=write
name=fiotest
blocksize=8k
filename=/mnt/pve/test/write
size=1g
ioengine=libaio
iodepth=32
numjobs=1
runtime=60
direct=1

Результат
fiotest: (g=0): rw=write, bs=(R) 8192B-8192B, (W) 8192B-8192B, (T) 8192B-8192B, ioengine=libaio, iodepth=32
fio-3.28
Starting 1 process
Jobs: 1 (f=1): [W(1)][100.0%][w=11.0MiB/s][w=1409 IOPS][eta 00m:00s]
fiotest: (groupid=0, jobs=1): err= 0: pid=3588: Sat May  3 00:16:19 2025
  write: IOPS=1530, BW=12.0MiB/s (12.5MB/s)(718MiB/60022msec); 0 zone resets
    slat (usec): min=3, max=141739, avg=94.73, stdev=1480.44
    clat (msec): min=2, max=262, avg=20.81, stdev=14.28
     lat (msec): min=2, max=262, avg=20.91, stdev=14.27
    clat percentiles (msec):
     |  1.00th=[    4],  5.00th=[    8], 10.00th=[   12], 20.00th=[   14],
     | 30.00th=[   16], 40.00th=[   17], 50.00th=[   18], 60.00th=[   20],
     | 70.00th=[   23], 80.00th=[   26], 90.00th=[   33], 95.00th=[   40],
     | 99.00th=[   69], 99.50th=[   95], 99.90th=[  203], 99.95th=[  226],
     | 99.99th=[  247]
   bw (  KiB/s): min= 5584, max=17216, per=99.85%, avg=12226.15, stdev=2529.45, samples=119
   iops        : min=  698, max= 2152, avg=1528.27, stdev=316.18, samples=119
  lat (msec)   : 4=1.24%, 10=6.83%, 20=52.96%, 50=36.68%, 100=1.86%
  lat (msec)   : 250=0.43%, 500=0.01%
  cpu          : usr=0.48%, sys=1.47%, ctx=68734, majf=0, minf=10
  IO depths    : 1=0.1%, 2=0.1%, 4=0.1%, 8=0.1%, 16=0.1%, 32=100.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.1%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,91862,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=32

Run status group 0 (all jobs):
  WRITE: bw=12.0MiB/s (12.5MB/s), 12.0MiB/s-12.0MiB/s (12.5MB/s-12.5MB/s), io=718MiB (753MB), run=60022-60022msec

Disk stats (read/write):
    dm-0: ios=126/98119, merge=0/0, ticks=3940/1857428, in_queue=1861368, util=99.31%, aggrios=126/96396, aggrmerge=0/2709, aggrticks=3928/1803591, aggrin_queue=1807713, aggrutil=99.23%
  sda: ios=126/96396, merge=0/2709, ticks=3928/1803591, in_queue=1807713, util=99.23%

конфиг 
[fiotest]
rw=write
name=fiotest
blocksize=8k
filename=/mnt/pve/test/write
size=1g
ioengine=libaio
iodepth=1
numjobs=1
runtime=60
direct=1

Результат
fiotest: (g=0): rw=write, bs=(R) 8192B-8192B, (W) 8192B-8192B, (T) 8192B-8192B, ioengine=libaio, iodepth=1
fio-3.28
Starting 1 process
Jobs: 1 (f=1): [W(1)][100.0%][w=1632KiB/s][w=204 IOPS][eta 00m:00s]
fiotest: (groupid=0, jobs=1): err= 0: pid=3616: Sat May  3 00:18:47 2025
  write: IOPS=282, BW=2258KiB/s (2312kB/s)(132MiB/60002msec); 0 zone resets
    slat (usec): min=6, max=42146, avg=91.13, stdev=759.96
    clat (usec): min=1609, max=285038, avg=3450.64, stdev=5465.66
     lat (usec): min=1617, max=285046, avg=3541.91, stdev=5565.78
    clat percentiles (usec):
     |  1.00th=[  1778],  5.00th=[  1909], 10.00th=[  2008], 20.00th=[  2147],
     | 30.00th=[  2278], 40.00th=[  2409], 50.00th=[  2573], 60.00th=[  2802],
     | 70.00th=[  3130], 80.00th=[  3916], 90.00th=[  5407], 95.00th=[  6980],
     | 99.00th=[ 11338], 99.50th=[ 16581], 99.90th=[ 83362], 99.95th=[124257],
     | 99.99th=[238027]
   bw (  KiB/s): min=  656, max= 3552, per=100.00%, avg=2266.08, stdev=760.91, samples=119
   iops        : min=   82, max=  444, avg=283.26, stdev=95.11, samples=119
  lat (msec)   : 2=9.96%, 4=70.89%, 10=17.68%, 20=1.12%, 50=0.21%
  lat (msec)   : 100=0.08%, 250=0.06%, 500=0.01%
  cpu          : usr=0.12%, sys=0.26%, ctx=17491, majf=0, minf=12
  IO depths    : 1=100.0%, 2=0.0%, 4=0.0%, 8=0.0%, 16=0.0%, 32=0.0%, >=64=0.0%
     submit    : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     complete  : 0=0.0%, 4=100.0%, 8=0.0%, 16=0.0%, 32=0.0%, 64=0.0%, >=64=0.0%
     issued rwts: total=0,16936,0,0 short=0,0,0,0 dropped=0,0,0,0
     latency   : target=0, window=0, percentile=100.00%, depth=1

Run status group 0 (all jobs):
  WRITE: bw=2258KiB/s (2312kB/s), 2258KiB/s-2258KiB/s (2312kB/s-2312kB/s), io=132MiB (139MB), run=60002-60002msec

Disk stats (read/write):
    dm-0: ios=220/23472, merge=0/0, ticks=2652/93376, in_queue=96028, util=97.68%, aggrios=220/21785, aggrmerge=0/2623, aggrticks=2622/79363, aggrin_queue=82138, aggrutil=97.58%
  sda: ios=220/21785, merge=0/2623, ticks=2622/79363, in_queue=82138, util=97.58%