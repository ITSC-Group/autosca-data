# Experiment cnblogscom500
## Date
Fri Jul 23 11:27:24 CEST 2021
## Host
machina
## Command Line Parameters
--host cnblogs.com --tag cnblogscom500 --tlsattacker --datasetfolder /home/datasets --clientarguments --repetitions 500 --timeout 3000 --skip --noskip
## Output Folder
/home/datasets/2021-07-23-cnblogscom500
## Prototype Version
git commit 1701321
on branch main

# Dataset generation
## Server Hostname/IP and Port
cnblogs.com:443
## Capturing network traffic
From and to cnblogs.com
On interface enp3s0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect cnblogs.com:443 --folder "/home/datasets/2021-07-23-cnblogscom500" --repetitions 500 --timeout 3000 --skip --noskip 2>&1 | tee "/home/datasets/2021-07-23-cnblogscom500/TLS Attacker.log"
## Execution Time
631 seconds
# Feature Extraction
## Execution Time
14 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
230 seconds
