---
title: Browser Real User Monitoring (BRUM)
time: 2 minutes
weight: 3
description: In this Learning Lab you learn how to use AppDynamics to monitor the health of your browser-based application.
---


## Browser Real User Monitoring

## Introduction

AppDynamics is a full-stack performance monitoring solution for your critical business applications that offers the following features:

*   Consistent end-to-end application monitoring, regardless of environment, traditional, hybrid, or cloud-native.
*   Accelerated cloud migration and enterprise-grade, end-to-end insights for your applications regardless of where they are deployed.
*   Unified monitoring that enables you to quickly resolve performance issues before they become business problems, with three clicks to root cause.

You can optimize the total cost of ownership by leveraging existing personnel, processes, and training on AppDynamics platform for traditional, cloud, or hybrid deployments.

## Objectives 
In this Learning Lab you learn how to use AppDynamics to monitor the health of your browser-based application.

When you have completed this lab, you will be able to:

- Create a browser application in the Controller
- Configure the Browser Real User Monitoring (BRUM) agent to monitor your web application’s health.
- Troubleshoot performance issues and find the root cause, whether it occurs on the browser side or the server side of the transaction.


## Workshop Environment

The workshop environment has two hosts:

- The first host is where you installed the AppDynamics Platform and runs the AppDynamics Controller and will be referred to from this point on as the **Controller VM**.
- The second host runs the Supercar Trader application used in the labs. It will be the host where you will install the AppDynamics agents and will be referred to from this point on as the **Application VM**.

## Controller
You will be using the AppDynamics SE Lab Controller for this workshop. 
[AppDynamics SE Lab](https://se-lab.saas.appdynamics.com/controller/)

![Controller](images/controller-vm.png)


## Application VM
Supercar Trader is a Java-based Web Application

The purpose of Supercar-Trader collection is to generate dynamic traffic (business transactions) for AppDynamics Controller.

![Application VM](images/application-vm.png)

