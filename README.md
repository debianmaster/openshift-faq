## Installation

1)  `The connection to the server master:8443 was refused - did you specify the right host or port?`   

```sh
TASK [openshift_examples : Import Centos Image streams] ***************************************************************************************
fatal: [master.cloud.example.com]: FAILED! => {
   "changed": false, 
   "cmd": [
       "/usr/local/bin/oc", 
       "create", 
       "-n", 
       "openshift", 
       "-f", 
       "/etc/origin/examples/image-streams/image-streams-centos7.json"
   ], 
   "delta": "0:00:00.184604", 
   "end": "2017-05-11 13:00:57.471839", 
   "failed": true, 
   "failed_when_result": true, 
   "rc": 1, 
   "start": "2017-05-11 13:00:57.287235"
}

STDERR:

The connection to the server master:8443 was refused - did you specify the right host or port?
```
Ans:

```sh
Check if you origin-master process if working  
```
## Architecture

## Storage

## Networking
