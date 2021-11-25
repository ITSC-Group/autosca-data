# Experiment ciscoace
## Date
Sat Jan 30 14:42:43 CET 2021
## Host
machina
## Command Line Parameters
--name imitation-server:6.0 --tag cisco_ace --docker --tlsattacker --port 44501 --datasetfolder /home/datasets --clientarguments --repetitions 500 --noskip --wait 500 --serverarguments --configFile=/config/base.conf --configFile=/config/cisco_ace.conf
## Output Folder
/home/datasets/2021-01-30-ciscoace
## Prototype Version
git commit 4b58846
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=ciscoace -p 44501:4433  imitation-server:6.0 --configFile=/config/base.conf --configFile=/config/cisco_ace.conf
## Server Hostname/IP and Port
localhost:44501
## Capturing network traffic
From and to 172.17.0.2
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44501 --folder "/home/datasets/2021-01-30-ciscoace" --repetitions 500 --noskip --wait 500 2>&1 | tee "/home/datasets/2021-01-30-ciscoace/TLS Attacker.log"
## Execution Time
300 seconds
# Feature Extraction
## Execution Time
14 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
399 seconds
