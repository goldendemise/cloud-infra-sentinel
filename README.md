# cloud-infra-sentinel
simple infrastructure monitoring

## How will this work?
A system service will periodically gather metrics for CPU, disk utilization, and memory utilization.
Might also be nice to search for IOWAIT and/or inode utilization

Configuration options will include:
1) Where to POST metrics
2) Where to log metrics locally (if applicable)
3) How much local data to retain
4) Failure behavior
5) Frequency of metric collection
6) Frequency of sending metrics

It might be useful to parse information from sysstat related tools ultimately, but initially this will only measure disk utilization, memory utilization, and CPU load
