# cloud-infra-sentinel
simple infrastructure monitoring

## How will this work?
A systemd service will periodically gather metrics for CPU, disk utilization, and memory utilization
Specifically, the metrics sent in JSON format will include:
load average(`os.loadavg()`) along with  number of cores (via `os.cpus().length`)
CPU utilization (acute)
Free memory and total memory (making this human readable should be handled by the metrics recipient. from `os.freemem()` and `os.totalmem()` respectively)
Disk space used and total disk space (per device, aggregates to be handled by the server. probably some combination of system `df` and `du`, probably with a separate `-h` for each returned as well)


Configuration options will include:
1) Where to POST metrics
2) Where to log metrics locally (if applicable)
3) How much local data to retain
4) Failure behavior
5) Frequency of metric collection
6) Frequency of sending metrics


