---
title: "Checking Status"
weight: 15
---

To check on the status of your job, you will use the `qstat`  and `qdel` command:

| Commands                      | Functions                                    |
| ----------------------------- | -------------------------------------------- |
| `qstat`                       | Lists jobs in queue                          |
| `qstat –q <queuename>`        | Lists the status of all queues               |
| `qstat -n`                    | Lists jobs and nodes they are assigned to    |
| `qdel <jobid>`                | Delete a specific job                        |
| `qstat –u <username>`         | Lists a user's jobs                          |
| `qstat -f`                    | Prints all info about all jobs               |
| `qstat -f XXXX`               | Prints all info about job XXXX               |
| `qstat -n`                    | Displays nodes allocated to any running jobs |
| `qstat -Q`                    | Displays status of queues                    |
|                               |                                              |
| `qdel <jobid>`                | Delete a specific job                        |
| `qdel $(qselect -u AccessID)` | Delete all of a user's jobs                  |