# Experiment damnvulnerableopensslserverfast
## Date
Thu Jan 14 15:32:36 CET 2021
## Host
machina
## Command Line Parameters
--tag damnvulnerableopensslserver-fast --name apollolv/damnvulnerableopenssl-server --docker --tlsattacker --port 44451 --datasetfolder /home/datasets --clientarguments --repetitions 50000 --skip --noskip
## Output Folder
/home/datasets/2021-01-14-damnvulnerableopensslserverfast
## Prototype Version
git commit 9116e4b
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=damnvulnerableopensslserverfast -p 44451:4433  apollolv/damnvulnerableopenssl-server 
## Server Hostname/IP and Port
localhost:44451
## Capturing network traffic
From and to 172.17.0.3
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44451 --folder "/home/datasets/2021-01-14-damnvulnerableopensslserverfast" --repetitions 50000 --skip --noskip | tee "/home/datasets/2021-01-14-damnvulnerableopensslserverfast/TLS Attacker.log"
## Execution Time
1643 seconds
# Feature Extraction
## Execution Time
1836 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
2640 seconds
