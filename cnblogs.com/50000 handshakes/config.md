# Experiment 20210412cnblogscom
## Date
Mon Apr 12 12:05:52 CEST 2021
## Host
machina
## Command Line Parameters
--host cnblogs.com --tag 2021-04-12-cnblogscom --tlsattacker --datasetfolder /home/datasets --clientarguments --repetitions 50000 --timeout 3000 --skip --noskip
## Output Folder
/home/datasets/20210412cnblogscom
## Prototype Version
git commit e8293a9
on branch master

# Dataset generation
## Server Hostname/IP and Port
cnblogs.com:443
## Capturing network traffic
From and to cnblogs.com
On interface enp3s0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect cnblogs.com:443 --folder "/home/datasets/20210412cnblogscom" --repetitions 50000 --timeout 3000 --skip --noskip 2>&1 | tee "/home/datasets/20210412cnblogscom/TLS Attacker.log"
## Execution Time
26246 seconds
# Feature Extraction
## Execution Time
704 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
1752 seconds
