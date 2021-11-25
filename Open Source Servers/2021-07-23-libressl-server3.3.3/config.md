# Experiment libressl-server3.3.3
## Date
Fri Jul 23 11:08:41 CEST 2021
## Host
machina
## Command Line Parameters
--name libressl-server:3.3.3 --docker --tlsattacker --port 44661 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -accept 4433 -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Output Folder
/home/datasets/2021-07-23-libressl-server3.3.3
## Prototype Version
git commit 1701321
on branch main

# Dataset generation
## Docker Command
docker run -it --rm -d --name=libressl-server3.3.3 -p 44661:4433 -v cert-data:/cert/:ro,nocopy libressl-server:3.3.3 -accept 4433 -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Server Hostname/IP and Port
localhost:44661
## Capturing network traffic
From and to 172.17.0.7
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44661 --folder "/home/datasets/2021-07-23-libressl-server3.3.3" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-07-23-libressl-server3.3.3/TLS Attacker.log"
## Execution Time
2016 seconds
# Feature Extraction
## Execution Time
2920 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
14174 seconds
