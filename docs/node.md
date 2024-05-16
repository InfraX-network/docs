---
title: Node
summary: A Node is the working unit of the InfraX network. It is a computer that is connected to the network and is used to execute user created Jobs against active Apps.
author: Kyle Dougan
date: 2024-04-30
tags: [node, infraX, network]
---

A Node is the working unit of the InfraX network. It is a computer that is connected to the network and is used to execute user created [Jobs](job.md) against active [Apps](app.md).

## Getting Started

To get started with contributing to the InfraX network as a node supplier, you will need to install and run the InfraX Node software on your computer. You can download the latest version of the software from the public [github repository](https://github.com/wegfawefgawefg/infrax-gpu-router-backend).

## Installation

To install the InfraX Node software, follow these steps:

1. Clone the repository to your local machine.
2. Edit the `config.toml` file to match your information.
3. Run the `install.sh` script to install the necessary dependencies.
4. Run the `start.sh` script to start the InfraX Node software.
5. Your node is now connected to the InfraX network and ready to install Apps and receive Jobs.

## Usage

Once your node is connected to the InfraX network, requests to install Apps and run Jobs will be sent to your node. You can view the status of your node and the Jobs that are currently running by visiting the InfraX dashboard.

## Updating

To update the InfraX Node software, simply run:

```bash
sudo ./manage.sh restart
```

This will pull the latest version of the software from the repository and restart the node.

```bash
devop@Infrax-Test-Node-1:~/infrax_node$ sudo ./manage.sh update
Already up to date.
  infrax.service                     loaded    active running InfraX Node service
  infrax.service                     loaded    active running InfraX Node service
  infrax.service                     loaded    active running InfraX Node service
● infrax.service - InfraX Node service
     Loaded: loaded (/etc/systemd/system/infrax.service; enabled; preset: enabled)
     Active: active (running) since Thu 2024-05-16 07:45:08 UTC; 52ms ago
   Main PID: 69945 (python3)
      Tasks: 1 (limit: 1092)
     Memory: 4.9M
        CPU: 20ms
     CGroup: /system.slice/infrax.service
             └─69945 /home/devop/infrax_node/.venv/bin/python3 -m uvicorn infrax_node.main:app --host 0.0.0.0 --port 8420

May 16 07:45:08 Infrax-Test-Node-1 systemd[1]: Started infrax.service - InfraX Node service.
```
