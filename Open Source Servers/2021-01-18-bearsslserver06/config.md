# Experiment bearsslserver06
## Date
Mon Jan 18 13:19:12 CET 2021
## Host
machina
## Command Line Parameters
--name bearssl-server:0.6 --docker --tlsattacker --port 44671 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -p 4433 -cert /cert/rsa2048cert.pem -key /cert/rsa2048key.pem
## Output Folder
/home/datasets/2021-01-18-bearsslserver06
## Prototype Version
git commit c326ff8
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=bearsslserver06 -p 44671:4433 -v cert-data:/cert/:ro,nocopy bearssl-server:0.6 -p 4433 -cert /cert/rsa2048cert.pem -key /cert/rsa2048key.pem
## Server Hostname/IP and Port
localhost:44671
## Capturing network traffic
From and to 172.17.0.3
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44671 --folder "/home/datasets/2021-01-18-bearsslserver06" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-01-18-bearsslserver06/TLS Attacker.log"
## Execution Time
2336 seconds
# Feature Extraction
## Execution Time
1753 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
1874 seconds
