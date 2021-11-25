# Experiment botanserver2173
## Date
Mon Jan 18 15:22:51 CET 2021
## Host
machina
## Command Line Parameters
--name botan-server:2.17.3 --docker --tlsattacker --port 44681 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments /cert/rsa2048cert.pem /cert/rsa2048key.pem --port=4433 --policy=/compat.txt
## Output Folder
/home/datasets/2021-01-18-botanserver2173
## Prototype Version
git commit c326ff8
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=botanserver2173 -p 44681:4433 -v cert-data:/cert/:ro,nocopy botan-server:2.17.3 /cert/rsa2048cert.pem /cert/rsa2048key.pem --port=4433 --policy=/compat.txt
## Server Hostname/IP and Port
localhost:44681
## Capturing network traffic
From and to 172.17.0.6
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44681 --folder "/home/datasets/2021-01-18-botanserver2173" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-01-18-botanserver2173/TLS Attacker.log"
## Execution Time
2431 seconds
# Feature Extraction
## Execution Time
2050 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
1941 seconds
