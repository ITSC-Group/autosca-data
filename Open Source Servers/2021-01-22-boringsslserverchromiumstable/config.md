# Experiment boringsslserverchromiumstable
## Date
Fri Jan 22 18:06:03 CET 2021
## Host
machina
## Command Line Parameters
--name boringssl-server:chromium-stable --docker --tlsattacker --port 44651 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -accept 4433 -cert /cert/rsa2048cert.pem -key /cert/rsa2048key.pem -loop
## Output Folder
/home/datasets/2021-01-22-boringsslserverchromiumstable
## Prototype Version
git commit 6b7ace2
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=boringsslserverchromiumstable -p 44651:4433 -v cert-data:/cert/:ro,nocopy boringssl-server:chromium-stable -accept 4433 -cert /cert/rsa2048cert.pem -key /cert/rsa2048key.pem -loop
## Server Hostname/IP and Port
localhost:44651
## Capturing network traffic
From and to 172.17.0.3
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44651 --folder "/home/datasets/2021-01-22-boringsslserverchromiumstable" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-01-22-boringsslserverchromiumstable/TLS Attacker.log"
## Execution Time
2197 seconds
# Feature Extraction
## Execution Time
1908 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
2485 seconds
