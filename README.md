# Apache Spark Standalone Cluster PostgreSQL on Docker

## Summary 

- [Introduction](#introduction)
- [Seção 2](#seção-2)
- [Seção 3](#seção-3)

## Introduction

This project was built with the aim of showing how a distributed environment can be highly powerful in situations involving data analysis with the appropriate tools for use, the project has the intention of showing that dealing with large volumes of data in highly scalable and Resilient systems can become a much more efficient and productive task in real workload situations. Using tools such as **Jupyter Notebook**, **Spark Clusters** and **PostgreSQL** further helps the knowledge of how each real task with data works in a production line.


## ETL (Extract, Transform and Load)

In this Project we use Clusters (Master, Worker) as ETL processes, an extremely powerful and versatile tool (can be worked on involving scalability with tools such as Kubernetes and cloud applications), with Spark we can create extremely efficient and performant ETL workloads.

> **Note:** To learn more about ETL [Click Here](https://www.oracle.com/ph/integration/what-is-etl/).


## Requirements and Recommendations

For a better experience and performance, it is recommended that the application be run on Ubuntu Linux OS, for compatibility and performance reasons.
>**Note:** You can running this application in OS like Window and macOS without problems.

## Have Docker and Docker-Compose Installed on your Machine 

If don't have installed docker your machine, you can install easily as follows

```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

```bash
sudo docker run hello-world
```

### Installing Docker-Compose

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/{VERSION}/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```bash
sudo chmod +x /usr/local/bin/docker-compose
```

```bash
docker-compose --version
```

If necessary, you can add your user to the docker group to run Docker commands without using `sudo`.

```bash
sudo usermod -aG docker $USER
```
## Starting Docker Containers

To initialize docker containers, you must be in the project's root directory and then execute:

```bash
docker-compose up
```

detached mode:

```bash
docker-compose up -d
```











