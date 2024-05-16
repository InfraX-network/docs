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

!!! note
    The InfraX Node software is designed to run on Linux based operating systems. If you are using a different operating system, you may need to set up a virtual machine or container to run the software.

To install the InfraX Node software, follow these steps:

1. Clone the repository to your local machine.
2. Edit the `config.toml` file to match your information.
3. Run the `install.sh` script to install the necessary dependencies and start the InfraX Node service.
4. Your node is now connected to the InfraX network and ready to install Apps and receive Jobs.

!!! warning
    Because the InfraX Node software is designed to accept external requests, it is important to ensure that your firewall settings allow incoming connections on the specified port (default `external_port=8420`). If you are running the software on a cloud server, you may need to configure the security group settings to allow incoming connections on the specified port.

## Usage

Once your node is connected to the InfraX network, requests to install Apps and run Jobs will be sent to your node. You can view the status of your node and the Jobs that are currently running by visiting the InfraX dashboard.

## Mangement

The InfraX Node software comes with a management script that can be used to update the software and restart the node. To update the software, run the following command:

```bash
sudo ./manage.sh update
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

Additional commands can be found by running the following command:

```bash
sudo ./manage.sh help
```

## Conclusion

Nodes are the backbone of the InfraX network and are essential for the execution of Jobs and Apps. By installing the InfraX Node software on your computer, you can contribute to the network and earn rewards for your work.
