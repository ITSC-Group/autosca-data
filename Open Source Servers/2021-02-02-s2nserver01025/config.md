# Experiment s2nserver01025
## Date
Di 2. Feb 23:24:03 CET 2021
## Host
machina
## Command Line Parameters
--name s2n-server:0.10.25 --docker --tlsattacker --port 44671 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --timeout 200 --serverarguments 0.0.0.0 4433 --cert /cert/rsa2048certs2n.pem --key /cert/rsa2048key.pem --parallelize
## Output Folder
/home/datasets/2021-02-02-s2nserver01025
## Prototype Version
git commit 90b0123
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=s2nserver01025 -p 44671:4433 -v cert-data:/cert/:ro,nocopy s2n-server:0.10.25 0.0.0.0 4433 --cert /cert/rsa2048certs2n.pem --key /cert/rsa2048key.pem --parallelize
## Server Hostname/IP and Port
localhost:44671
## Capturing network traffic
From and to 172.17.0.2
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44671 --folder "/home/datasets/2021-02-02-s2nserver01025" --repetitions 50000 --skip --noskip --timeout 200 2>&1 | tee "/home/datasets/2021-02-02-s2nserver01025/TLS Attacker.log"
## Execution Time
10814 seconds
# Feature Extraction
## Execution Time
2223 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
1534 seconds
