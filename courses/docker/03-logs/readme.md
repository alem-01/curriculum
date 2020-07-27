# La-La-Logs

Docker allows you to views logs of running applications and view stats of container I/O, CPU usage.

## Exercises

1. **Logs since 1 hour ago**

File: `logs1hour.sh`

Write script that saves to file with following name `$(date +\%Y-\%m-\%dT\%H:\%M).logs` 
logs of container named `web-app` since 2 hours and 30 minutes. 

```bash
sh logs1hour.sh
ls
> logs1hour.sh  stats.sh  2020-07-22T16:20.logs
```
___

2. **Stats, Now!**

File: `stats.sh`

Write script that outputs first result of container stats including exited ones to file 
`$(date +\%Y-\%m-\%dT\%H:\%M).stats`.

```bash
sh stats.sh
ls
> logs1hour.sh  stats.sh  2020-07-22T16:20.logs  2020-07-22T16:22.stats
```
