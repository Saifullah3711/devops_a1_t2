# Assignment 1 Task 2
#### Run the previous docker at background for specific port binding. 
* ```docker run -d -p 2010:80 docker-image-a1-p1```

## Checking different commands and its outputs
* ```docker ps``` 
* CONTAINER ID   IMAGE                COMMAND           CREATED          STATUS          PORTS                  NAMES
80bde14ba6c4   docker-image-a1-p1   "python app.py"   9 seconds ago    Up 8 seconds    0.0.0.0:8080->80/tcp   unruffled_cartwright
18a0784698be   docker-image-a1-p1   "python app.py"   41 minutes ago   Up 41 minutes   0.0.0.0:2010->80/tcp   jovial_khayyam

* ```docker stop```
* CONTAINER ID   IMAGE                COMMAND           CREATED          STATUS          PORTS                  NAMES
18a0784698be   docker-image-a1-p1   "python app.py"   43 minutes ago   Up 43 minutes   0.0.0.0:2010->80/tcp   jovial_khayyam

* ```docker rm 80bde14ba6c4```
* 80bde14ba6c4

* ```docker logs```
* 2023-11-03 15:58:55 INFO:     Started server process [1]
2023-11-03 15:58:55 INFO:     Waiting for application startup.
2023-11-03 15:58:55 INFO:     Application startup complete.
2023-11-03 15:58:55 INFO:     Uvicorn running on http://0.0.0.0:2010 (Press CTRL+C to quit)
* ```docker inspect docker-image-a1-p1```
* [
    {
        "Id": "sha256:2b91c9c8c0c32b132a53fa689621c0343ffe3ea86f6721d7c987fe3252a2f506",
        "RepoTags": [
            "docker-image-a1-p1:latest",
            "saifullah3711/a_1_t_1:latest"
        ],
        "RepoDigests": [
            "saifullah3711/a_1_t_1@sha256:91cc552da0db85c7d791bb584e03b1bb5dc8cc693e7ad43a6e12e685e1629938"
        ],
        "Parent": "",
        "Comment": "buildkit.dockerfile.v0",
        "Created": "2023-11-03T07:26:58.850299072Z",
        "Container": "",
        "ContainerConfig": {
            "Hostname": "",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": null,
            "Cmd": null,
            "Image": "",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": null,
            "OnBuild": null,
            "Labels": null
        },
        "DockerVersion": "",
        "Author": "",
        "Config": {
            "Hostname": "",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "LANG=C.UTF-8",
                "GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305",
                "PYTHON_VERSION=3.12.0",
                "PYTHON_PIP_VERSION=23.2.1",
                "PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c6add47b0abf67511cdfb4734771cbab403af062/public/get-pip.py",
                "PYTHON_GET_PIP_SHA256=22b849a10f86f5ddf7ce148ca2a31214504ee6c83ef626840fde6e5dcd809d11"
            ],
            "Cmd": null,
            "ArgsEscaped": true,
            "Image": "",
            "Volumes": null,
            "WorkingDir": "",
            "Entrypoint": [
                "python",
                "app.py"
            ],
            "OnBuild": null,
            "Labels": null
        },
        "Architecture": "amd64",
        "Os": "linux",
        "Size": 1045090897,
        "VirtualSize": 1045090897,
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/48kfa7gdj3hl59kb7rgwjt5dt/diff:/var/lib/docker/overlay2/apexos3ook7rbuyhr77e9toum/diff:/var/lib/docker/overlay2/72aa66c15a1cb77677410469506c3dfabdb4cbb1e13b01ad02fdf74661681080/diff:/var/lib/docker/overlay2/ba61967608757251bb252813690effcbe967d5d65d57c3a0f1ddb502aacadc84/diff:/var/lib/docker/overlay2/5cfd5c916965a14e5b289749a82227fd1063ca218ed95cd1be7cf921b6a5727a/diff:/var/lib/docker/overlay2/3c626c267befae9cb672cf1896938b641bb2992ff4ffb8b42d9f7ad42d704f18/diff:/var/lib/docker/overlay2/59dd73857ba4312ef1aaf97e8e5c4c0a0acf04a273e1b81a573a7f5d87ad2a34/diff:/var/lib/docker/overlay2/50f778e8527f4db9f4498ee93065e67bdc10cb46dfe6e39e09e1be71cce083e2/diff:/var/lib/docker/overlay2/6b85249b57804cfcb95d37618286ddce24749da4d96c9a690416cba1196b3fd4/diff:/var/lib/docker/overlay2/b96b5bf7d0209eebb3a5c22a7282485607e98aa131e3598f4666627f5a730825/diff",
                "MergedDir": "/var/lib/docker/overlay2/6e5jakvpn280sht9nai0kvp03/merged",
                "UpperDir": "/var/lib/docker/overlay2/6e5jakvpn280sht9nai0kvp03/diff",
                "WorkDir": "/var/lib/docker/overlay2/6e5jakvpn280sht9nai0kvp03/work"
            },
            "Name": "overlay2"
        },
        "RootFS": {
            "Type": "layers",
            "Layers": [
                "sha256:1777ac7d307bcbda4fe79323a921eda8d39d97513677ecda31b82244e7876520",
                "sha256:29e49b59edda8f520e3289a0df2f1aedc8c6774212c2b430359c9603310a3838",
                "sha256:266def75d28e675320db1c5d2870ff3ed8f2e7a78537a35fe495fbff6baa9dc7",
                "sha256:12b956927ba2b8fd3b59cd4db0f17068758e60eeb710ed307a0b006ddbf290b5",
                "sha256:86e50e0709eebc0f2f9de74341dd7330faa7cfe38a28d2cb2549d9b4629892f5",
                "sha256:ac630c4fd9602de2d6c99123caadba88885101582787ec1df5b2edee59834db2",
                "sha256:619584b251c8772c9d769a0fe95991e66785da834933e9ee9e49572422013cf3",
                "sha256:701d0b971f5f2c26b39eef7be204ffb84e491270a2181c115f952a1573f9e024",
                "sha256:151e4a6a1981b4d12283956019ab03cb218421333a1291f4cd84d41192deade0",
                "sha256:7f6fe586a0a52955ab37f4175ae37755a6a40767630e9d5bd6cc4e8bb7296767",
                "sha256:023800d05c10989dbf34ac26f12fc3819b51501e66da8ff0f074d44ef609f6cb"
            ]
        },
        "Metadata": {
            "LastTagTime": "2023-11-03T10:56:18.89422315Z"
        }
    }
]


* ``` docker exec 7424b39d288e echo "hello, assignemnt 1"``
* hello, assignemnt 1

* ```docker attach b30c2d570ebb```
* INFO:     Shutting down
INFO:     Waiting for application shutdown.
INFO:     Application shutdown complete.
INFO:     Finished server process [1]

* ```docker commit b30c2d570ebb```
* sha256:d68b747579677035f18bcded52d1f4a7cb2e7d9f3ea46ec40865f70f9b247616

* ```docker cp requirements.txt b30c2d570ebb:/requirements.txt```
* Successfully copied 2.05kB to b30c2d570ebb:/requirements.txt
* ```docker stats b30c2d570ebb```

*CONTAINER ID   NAME            CPU %     MEM USAGE / LIMIT   MEM %     NET I/O   BLOCK I/O   PIDS
b30c2d570ebb   hopeful_kilby   0.00%     0B / 0B             0.00%     0B / 0B   0B / 0B     0

* ```docker top 7424b39d288e```
* UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                11770               11749               0                   10:56               ?                   00:00:05            python app.py

* ```docker start 9805e660e494```
* 9805e660e494

* ```docker pause 9805e660e494```
* 9805e660e494

* ```docker unpause 9805e660e494```
* 9805e660e494

* ```docker port 9805e660e494```
* docker port 9805e660e494

* ```docker update --memory 6m 9805e660e494```
* update the memoryswap at the same time

* ```docker restart 9805e660e494```
* 9805e660e494