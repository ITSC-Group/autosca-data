# Experiment 000081cnblogs.com
## Date
Fri Apr  9 14:55:18 CEST 2021
## Host
machina
## Command Line Parameters
--host cnblogs.com --tag 000081cnblogs.com --tlsattacker --datasetfolder /home/datasets/2021-04-08-alexa-500 --clientarguments --repetitions 500 --timeout 3000 --skip --noskip
## Output Folder
/home/datasets/2021-04-08-alexa-500/000081cnblogs.com
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
java -jar apps/ML-BleichenbacherGenerator.jar -connect cnblogs.com:443 --folder "/home/datasets/2021-04-08-alexa-500/000081cnblogs.com" --repetitions 500 --timeout 3000 --skip --noskip 2>&1 | tee "/home/datasets/2021-04-08-alexa-500/000081cnblogs.com/TLS Attacker.log"
## Execution Time
638 seconds
# Feature Extraction
## Execution Time
13 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
170 seconds
