# cloud-infra-sentinel
simple infrastructure monitoring

## How will this work?
A systemd service will periodically gather metrics for CPU, disk utilization, and memory utilization
Specifically, the metrics provided will include:
load average (along with  number of cores)
CPU utilization (acute)
Free memory and total memory (making this human readable should be handled by the metrics recipient)
Disk space used and total disk space (per device, aggregates to be handled by the server)


Configuration options will include:
1) Where to POST metrics
2) Where to log metrics locally (if applicable)
3) How much local data to retain
4) Failure behavior
5) Frequency of metric collection
6) Frequency of sending metrics

None of this should depend on system utilities. More research would be required to measure single threading issues and the like
