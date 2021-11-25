# Experiment openssl097aserver
## Date
Wed Jan  6 14:55:57 CET 2021
## Host
machina
## Command Line Parameters
--name openssl-0_9_7a-server --docker --tlsattacker --port 44442 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Output Folder
/home/datasets/2021-01-06-openssl097aserver
## Prototype Version
git commit 578c8e8
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=openssl097aserver -p 44442:4433 -v cert-data:/cert/:ro,nocopy openssl-0_9_7a-server -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Server Hostname/IP and Port
localhost:44442
## Capturing network traffic
From and to 172.17.0.3
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44442 --folder "/home/datasets/2021-01-06-openssl097aserver" --repetitions 50000 --skip --noskip | tee "/home/datasets/2021-01-06-openssl097aserver/TLS Attacker.log"
## Execution Time
3524 seconds
# Feature Extraction
## Execution Time
13668 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
30878 seconds
