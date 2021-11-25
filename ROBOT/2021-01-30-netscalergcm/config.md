# Experiment netscalergcm
## Date
Sat Jan 30 14:42:43 CET 2021
## Host
machina
## Command Line Parameters
--name imitation-server:6.0 --tag netscaler_gcm --docker --tlsattacker --port 44504 --datasetfolder /home/datasets --clientarguments --repetitions 500 --noskip --wait 500 --serverarguments --configFile=/config/base.conf --configFile=/config/netscaler_gcm.conf
## Output Folder
/home/datasets/2021-01-30-netscalergcm
## Prototype Version
git commit 4b58846
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=netscalergcm -p 44504:4433  imitation-server:6.0 --configFile=/config/base.conf --configFile=/config/netscaler_gcm.conf
## Server Hostname/IP and Port
localhost:44504
## Capturing network traffic
From and to 172.17.0.5
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44504 --folder "/home/datasets/2021-01-30-netscalergcm" --repetitions 500 --noskip --wait 500 2>&1 | tee "/home/datasets/2021-01-30-netscalergcm/TLS Attacker.log"
## Execution Time
290 seconds
# Feature Extraction
## Execution Time
10 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
400 seconds
