---
title: Install Database Agent
time: 2 minutes
weight: 3
description: In this exercise you will upload the database visiblity agent, unzip the downloaded file, and start the database visiblity agent.
---

The AppDynamics Database Agent is a standalone Java program that collects performance metrics about your database instances and database servers. You can deploy the Database Agent on any machine running Java 1.8 or higher. The machine must have network access to the AppDynamics Controller and the database instance that you want to be monitored.

A database agent running on a typical machine with 16 GB of memory can monitor about 25 databases. On larger machines, a database agent can monitor up to 200 databases.

In this exercise you will perform the following tasks:

- Upload the Database Visibility agent file to your Application VM
- Unzip the file into a specific directory on the file system
- Start the Database Visibility agent

## Upload Database Agent to Application VM

The process of uploading the Database agent file will vary depending on your workstation’s operating system. Copy the Database agent ZIP file either using SCP if your Desktop is MAC/Linux or using WinSCP if your Desktop is Windows.

## Install the Database Agent

- Create the directory structure where you will unzip the Database agent zip file.

```bash
cd /opt/appdynamics
mkdir dbagent
```

- Use the following commands to copy the Database Visibility agent zip file to the directory and unzip the file. The name of your Database Visibility agent file may be slightly different than the example below. (assumes you uploaded the zip file to the /tmp directory)

```bash
cp /tmp/db-agent-20.4.0.1730.zip /opt/appdynamics/dbagent/
cd /opt/appdynamics/dbagent
unzip db-agent-20.4.0.1730.zip
```

## Start the Database Visibility agent

Use the following commands to start the Database Visibility agent and verify that it started.

```bash
cd /opt/appdynamics/dbagent
nohup java -Dappdynamics.agent.maxMetrics=300000 -Ddbagent.name=DBMon-Lab-Agent -jar db-agent.jar &
ps -ef | grep db-agent
```

You should see output similar to the following image.

![Output](images/04-dbagent-install-03%20(1).png)

