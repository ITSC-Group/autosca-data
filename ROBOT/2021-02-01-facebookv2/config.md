# Experiment facebookv2
## Date
Mon Feb  1 14:30:25 CET 2021
## Host
machina
## Command Line Parameters
--name imitation-server:6.0 --tag facebook_v2 --docker --tlsattacker --port 44503 --datasetfolder /home/datasets --clientarguments --repetitions 500 --skip --wait 1500 --timeout 200 --serverarguments --configFile=/config/base.conf --configFile=/config/facebook_v2.conf
## Output Folder
/home/datasets/2021-02-01-facebookv2
## Prototype Version
git commit 4b58846
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=facebookv2 -p 44503:4433  imitation-server:6.0 --configFile=/config/base.conf --configFile=/config/facebook_v2.conf
## Server Hostname/IP and Port
localhost:44503
## Capturing network traffic
From and to 172.17.0.2
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44503 --folder "/home/datasets/2021-02-01-facebookv2" --repetitions 500 --skip --wait 1500 --timeout 200 2>&1 | tee "/home/datasets/2021-02-01-facebookv2/TLS Attacker.log"
## Execution Time
899 seconds
# Feature Extraction
## Execution Time
13 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
101 seconds
