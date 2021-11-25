# Experiment openssl-server1.1.1k
## Date
Fri Jul 23 10:58:36 CEST 2021
## Host
machina
## Command Line Parameters
--name openssl-server:1.1.1k --docker --tlsattacker --port 44441 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Output Folder
/home/datasets/2021-07-23-openssl-server1.1.1k
## Prototype Version
git commit 1701321
on branch main

# Dataset generation
## Docker Command
docker run -it --rm -d --name=openssl-server1.1.1k -p 44441:4433 -v cert-data:/cert/:ro,nocopy openssl-server:1.1.1k -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Server Hostname/IP and Port
localhost:44441
## Capturing network traffic
From and to 172.17.0.5
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44441 --folder "/home/datasets/2021-07-23-openssl-server1.1.1k" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-07-23-openssl-server1.1.1k/TLS Attacker.log"
## Execution Time
1974 seconds
# Feature Extraction
## Execution Time
2002 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
11485 seconds
