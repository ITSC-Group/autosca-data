# Experiment ocamltlsserver0128
## Date
Mon Jan 25 20:15:42 CET 2021
## Host
machina
## Command Line Parameters
--name ocamltls-server:0.12.8 --docker --tlsattacker --port 44691 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip
## Output Folder
/home/datasets/2021-01-25-ocamltlsserver0128
## Prototype Version
git commit 6b7ace2
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=ocamltlsserver0128 -p 44691:4433 -v cert-data:/cert/:ro,nocopy ocamltls-server:0.12.8 
## Server Hostname/IP and Port
localhost:44691
## Capturing network traffic
From and to 172.17.0.3
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44691 --folder "/home/datasets/2021-01-25-ocamltlsserver0128" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-01-25-ocamltlsserver0128/TLS Attacker.log"
## Execution Time
2195 seconds
# Feature Extraction
## Execution Time
1819 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
2202 seconds
