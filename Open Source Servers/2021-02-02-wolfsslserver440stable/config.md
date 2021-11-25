# Experiment wolfsslserver440stable
## Date
Tue Feb  2 22:22:39 CET 2021
## Host
machina
## Command Line Parameters
--name wolfssl-server:4.4.0-stable --docker --tlsattacker --port 44601 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments -p 4433 -c /cert/rsa2048cert.pem -k /cert/rsa2048key.pem -i -b -d -x -l TLS_RSA_WITH_3DES_EDE_CBC_SHA:TLS_RSA_WITH_AES_128_CBC_SHA:TLS_RSA_WITH_AES_128_CBC_SHA256:TLS_RSA_WITH_AES_256_CBC_SHA256
## Output Folder
/home/datasets/2021-02-02-wolfsslserver440stable
## Prototype Version
git commit 4b58846
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=wolfsslserver440stable -p 44601:4433 -v cert-data:/cert/:ro,nocopy wolfssl-server:4.4.0-stable -p 4433 -c /cert/rsa2048cert.pem -k /cert/rsa2048key.pem -i -b -d -x -l TLS_RSA_WITH_3DES_EDE_CBC_SHA:TLS_RSA_WITH_AES_128_CBC_SHA:TLS_RSA_WITH_AES_128_CBC_SHA256:TLS_RSA_WITH_AES_256_CBC_SHA256
## Server Hostname/IP and Port
localhost:44601
## Capturing network traffic
From and to 172.17.0.2
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44601 --folder "/home/datasets/2021-02-02-wolfsslserver440stable" --repetitions 50000 --skip --noskip 2>&1 | tee "/home/datasets/2021-02-02-wolfsslserver440stable/TLS Attacker.log"
## Execution Time
2135 seconds
# Feature Extraction
## Execution Time
2212 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
1692 seconds
