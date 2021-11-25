# Experiment gnutls-server3.7.2
## Date
Fri Jul 23 11:06:58 CEST 2021
## Host
machina
## Command Line Parameters
--name gnutls-server:3.7.2 --docker --tlsattacker --port 44621 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments --port=4433 --x509certfile=/cert/rsa2048cert.pem --x509keyfile=/cert/rsa2048key.pem --disable-client-cert
## Output Folder
/home/datasets/2021-07-23-gnutls-server3.7.2
## Prototype Version
git commit 1701321
on branch main

# Dataset generation
## Docker Command
docker run -it --rm -d --name=gnutls-server3.7.2 -p 44621:4433 -v cert-data:/cert/:ro,nocopy gnutls-server:3.7.2 --port=4433 --x509certfile=/cert/rsa2048cert.pem --x509keyfile=/cert/rsa2048key.pem --disable-client-cert
## Server Hostname/IP and Port
localhost:44621
## Capturing network traffic
From and to 172.17.0.6
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44621 --folder "/home/datasets/2021-07-23-gnutls-server3.7.2" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-07-23-gnutls-server3.7.2/TLS Attacker.log"
## Execution Time
2042 seconds
# Feature Extraction
## Execution Time
2322 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
13610 seconds
