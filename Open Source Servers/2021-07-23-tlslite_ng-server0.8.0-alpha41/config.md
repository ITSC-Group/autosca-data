# Experiment tlslite_ng-server0.8.0-alpha41
## Date
Fri Jul 23 17:52:43 CEST 2021
## Host
machina
## Command Line Parameters
--name tlslite_ng-server:0.8.0-alpha41 --docker --tlsattacker --port 44681 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -c /cert/rsa2048cert.pem -k /cert/rsa2048key.pem 0.0.0.0:4433
## Output Folder
/home/datasets/2021-07-23-tlslite_ng-server0.8.0-alpha41
## Prototype Version
git commit 1701321
on branch main

# Dataset generation
## Docker Command
docker run -it --rm -d --name=tlslite_ng-server0.8.0-alpha41 -p 44681:4433 -v cert-data:/cert/:ro,nocopy tlslite_ng-server:0.8.0-alpha41 -c /cert/rsa2048cert.pem -k /cert/rsa2048key.pem 0.0.0.0:4433
## Server Hostname/IP and Port
localhost:44681
## Capturing network traffic
From and to 172.17.0.5
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44681 --folder "/home/datasets/2021-07-23-tlslite_ng-server0.8.0-alpha41" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-07-23-tlslite_ng-server0.8.0-alpha41/TLS Attacker.log"
## Execution Time
2435 seconds
# Feature Extraction
## Execution Time
2012 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
5936 seconds
