# Experiment openssl097bserver
## Date
Mi 13. Jan 16:47:54 CET 2021
## Host
machina
## Command Line Parameters
--name openssl-0_9_7b-server --docker --tlsattacker --port 44443 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Output Folder
/home/datasets/2021-01-13-openssl097bserver
## Prototype Version
git commit ac4ef65
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=openssl097bserver -p 44443:4433 -v cert-data:/cert/:ro,nocopy openssl-0_9_7b-server -key /cert/rsa2048key.pem -cert /cert/rsa2048cert.pem
## Server Hostname/IP and Port
localhost:44443
## Capturing network traffic
From and to 172.17.0.5
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44443 --folder "/home/datasets/2021-01-13-openssl097bserver" --repetitions 50000 --skip --noskip | tee "/home/datasets/2021-01-13-openssl097bserver/TLS Attacker.log"
## Execution Time
2446 seconds
# Feature Extraction
## Execution Time
2102 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
2548 seconds
