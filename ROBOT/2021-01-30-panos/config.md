# Experiment panos
## Date
Sat Jan 30 14:42:43 CET 2021
## Host
machina
## Command Line Parameters
--name imitation-server:6.0 --tag pan_os --docker --tlsattacker --port 44505 --datasetfolder /home/datasets --clientarguments --repetitions 500 --noskip --wait 500 --serverarguments --configFile=/config/base.conf --configFile=/config/pan_os.conf
## Output Folder
/home/datasets/2021-01-30-panos
## Prototype Version
git commit 4b58846
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=panos -p 44505:4433  imitation-server:6.0 --configFile=/config/base.conf --configFile=/config/pan_os.conf
## Server Hostname/IP and Port
localhost:44505
## Capturing network traffic
From and to 172.17.0.6
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44505 --folder "/home/datasets/2021-01-30-panos" --repetitions 500 --noskip --wait 500 2>&1 | tee "/home/datasets/2021-01-30-panos/TLS Attacker.log"
## Execution Time
305 seconds
# Feature Extraction
## Execution Time
18 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
302 seconds
