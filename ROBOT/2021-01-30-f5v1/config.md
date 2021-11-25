# Experiment f5v1
## Date
Sat Jan 30 14:42:43 CET 2021
## Host
machina
## Command Line Parameters
--name imitation-server:6.0 --tag f5_v1 --docker --tlsattacker --port 44502 --datasetfolder /home/datasets --clientarguments --repetitions 500 --skip --wait 500 --serverarguments --configFile=/config/base.conf --configFile=/config/f5_v1.conf
## Output Folder
/home/datasets/2021-01-30-f5v1
## Prototype Version
git commit 4b58846
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=f5v1 -p 44502:4433  imitation-server:6.0 --configFile=/config/base.conf --configFile=/config/f5_v1.conf
## Server Hostname/IP and Port
localhost:44502
## Capturing network traffic
From and to 172.17.0.4
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44502 --folder "/home/datasets/2021-01-30-f5v1" --repetitions 500 --skip --wait 500 2>&1 | tee "/home/datasets/2021-01-30-f5v1/TLS Attacker.log"
## Execution Time
298 seconds
# Feature Extraction
## Execution Time
13 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
392 seconds
