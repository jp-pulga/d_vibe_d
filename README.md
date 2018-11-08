# Performace result

## DMD + release build
```
$ wrk -t18 -c400 -d30s http://127.0.0.1:8080/
Running 30s test @ http://127.0.0.1:8080/
  18 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    13.02ms   39.28ms   1.21s    99.18%
    Req/Sec     2.13k   516.95    11.07k    95.98%
  1128334 requests in 30.09s, 181.86MB read
Requests/sec:  37495.47
Transfer/sec:      6.04MB
```

## LDC + release build
```
$ wrk -t18 -c400 -d30s http://127.0.0.1:8080/
Running 30s test @ http://127.0.0.1:8080/
  18 threads and 400 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency     9.91ms   27.90ms 915.44ms   99.34%
    Req/Sec     2.67k   623.73    15.68k    94.32%
  1413325 requests in 30.09s, 227.79MB read
  Socket errors: connect 0, read 13, write 0, timeout 0
Requests/sec:  46967.21
Transfer/sec:      7.57MB
```