# Experiment opensslserver111i
## Date
Thu Jan 14 15:40:39 CET 2021
## Host
machina
## Command Line Parameters
--name openssl-server:1.1.1i --docker --tlsattacker --port 44441 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Output Folder
/home/datasets/2021-01-14-opensslserver111i
## Prototype Version
git commit 9116e4b
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=opensslserver111i -p 44441:4433 -v cert-data:/cert/:ro,nocopy openssl-server:1.1.1i -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Server Hostname/IP and Port
localhost:44441
## Capturing network traffic
From and to 172.17.0.5
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44441 --folder "/home/datasets/2021-01-14-opensslserver111i" --repetitions 50000 --skip --noskip | tee "/home/datasets/2021-01-14-opensslserver111i/TLS Attacker.log"
## Execution Time
2201 seconds
# Feature Extraction
## Execution Time
2497 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
2091 seconds
