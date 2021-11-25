# Experiment matrixssl-server4.3.0
## Date
Fri Jul 23 11:09:16 CEST 2021
## Host
machina
## Command Line Parameters
--name matrixssl-server:4.3.0 --docker --tlsattacker --port 44463 --datasetfolder /home/datasets --clientarguments --repetitions 50000 --skip --noskip
## Output Folder
/home/datasets/2021-07-23-matrixssl-server4.3.0
## Prototype Version
git commit 1701321
on branch main

# Dataset generation
## Docker Command
docker run -it --rm -d --name=matrixssl-server4.3.0 -p 44463:4433  matrixssl-server:4.3.0 
## Server Hostname/IP and Port
localhost:44463
## Capturing network traffic
From and to 172.17.0.8
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44463 --folder "/home/datasets/2021-07-23-matrixssl-server4.3.0" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-07-23-matrixssl-server4.3.0/TLS Attacker.log"
## Execution Time
2160 seconds
# Feature Extraction
## Execution Time
3080 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
13598 seconds
