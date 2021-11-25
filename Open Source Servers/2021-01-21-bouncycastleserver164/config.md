# Experiment bouncycastleserver164
## Date
Thu Jan 21 17:48:44 CET 2021
## Host
machina
## Command Line Parameters
--name bouncycastle-server:1.64 --docker --tlsattacker --port 44472 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments 4433 /cert/keys.jks password rsa2048 /cert/keys.jks password ec256
## Output Folder
/home/datasets/2021-01-21-bouncycastleserver164
## Prototype Version
git commit c326ff8
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=bouncycastleserver164 -p 44472:4433 -v cert-data:/cert/:ro,nocopy bouncycastle-server:1.64 4433 /cert/keys.jks password rsa2048 /cert/keys.jks password ec256
## Server Hostname/IP and Port
localhost:44472
## Capturing network traffic
From and to 172.17.0.6
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44472 --folder "/home/datasets/2021-01-21-bouncycastleserver164" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-01-21-bouncycastleserver164/TLS Attacker.log"
## Execution Time
2345 seconds
# Feature Extraction
## Execution Time
2125 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
3375 seconds
