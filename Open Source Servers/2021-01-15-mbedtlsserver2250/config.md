# Experiment mbedtlsserver2250
## Date
Fri Jan 15 11:26:47 CET 2021
## Host
machina
## Command Line Parameters
--name mbedtls-server:2.25.0 --docker --tlsattacker --port 44494 --datasetfolder /home/datasets --dockerarguments -v cert-data:/cert/:ro,nocopy --clientarguments --repetitions 50000 --skip --noskip --serverarguments crt_file=/cert/rsa2048cert.pem key_file=/cert/rsa2048key.pem server_port=4433
## Output Folder
/home/datasets/2021-01-15-mbedtlsserver2250
## Prototype Version
git commit c8c626b
on branch master

# Dataset generation
## Docker Command
docker run -it --rm -d --name=mbedtlsserver2250 -p 44494:4433 -v cert-data:/cert/:ro,nocopy mbedtls-server:2.25.0 crt_file=/cert/rsa2048cert.pem key_file=/cert/rsa2048key.pem server_port=4433
## Server Hostname/IP and Port
localhost:44494
## Capturing network traffic
From and to 172.17.0.3
On interface docker0
## Client Command
java -jar apps/ML-BleichenbacherGenerator.jar -connect localhost:44494 --folder "/home/datasets/2021-01-15-mbedtlsserver2250" --repetitions 50000 --skip --noskip | tee "/home/datasets/2021-01-15-mbedtlsserver2250/TLS Attacker.log"
## Execution Time
2334 seconds
# Feature Extraction
## Execution Time
1983 seconds
# Machine Learning
## Parameters
Doing 30 crossvalidation iterations
Doing 10 hyperparameter optimization iterations
## Execution Time
1754 seconds
