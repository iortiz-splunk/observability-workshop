---
title: Monitor Server Health
time: 2 minutes
weight: 4
description: In this exercise you will review several dashboards to monitor server health and navigate between server and application contexts.
---

In this exercise you will complete the following tasks:

- Review the Server Main dashboard
- Review the Server Processes dashboard
- Review the Server Volumes dashboard
- Review the Server Network dashboard
- Navigate between Server and Application contexts

## Review the Server Main Dashboard

Now that you have the Server Visibility Monitoring agent installed, let’s take a look at some of the features available in the Server Visibility module.

Navigate to the Servers list dashboard and drill into the servers main dashboard by following these steps.

1. Click the Servers tab on the top menu.
2. Check the checkbox on the left for the first server.
3. Click View Details.

You can read more about the Servers List dashboard here.

![Server Health](images/svm-dashboard-01.png)

You can now explore the server main dashboard. This dashboard enables you to perform the following tasks:

- See charts of key performance metrics for the selected monitored servers, including:
    -  Server availability
    - CPU, memory, and network usage percentages
    - Server properties
    - Disk, partition, and volume metrics
    - Top 10 processes consuming CPU resources and memory.

- Change the time period of the metrics displayed.
- See an assessment of the overall health of the server, as determined by whether any health rules have been violated.
- View Health Rule Status in the UI.
- See the hierarchy or grouping of the server as specified in the controller-info.xml file using the machine-path configuration property.
- Click on any point on a chart to see the metric value for that time.
- Find and switch to other Server Dashboards (pull-down menu next to server tier, top left).
- View an aggregate of the top 10 processes by CPU usage, and top 10 processes by memory.

You can read more about the Server Main dashboard [here](https://docs.appdynamics.com/appd/23.x/latest/en/infrastructure-visibility/server-visibility/monitor-your-servers-using-server-visibility/server-dashboard).

![Dashboard Example](images/svm-dashboard-02.png)
![Dashboard Example](images/svm-dashboard-03.png)

## Review the Server Processes Dashboard

1. Click the Processes tab.
2. Click View Options to select different data columns.

You can now explore the server processes dashboard. This dashboard enables you to perform the following tasks:

- View all the processes active during the selected time period. The processes are grouped by class as specified in the ServerMonitoring.yml file.
- View the full command line that started this process by hovering over the process entry in the Command Line column.
- Expand a process class to see the processes associated with that class.
- Use View Options to configure which columns to display in the chart.
- Change the time period of the metrics displayed.
- Sort the chart using the columns as a sorting key. You can not sort on sparkline charts: CPU Trend and Memory Trend.
- See CPU and Memory usage trends at a glance.

You can read more about the Server Processes dashboard [here](https://docs.appdynamics.com/appd/23.x/latest/en/infrastructure-visibility/server-visibility/monitor-your-servers-using-server-visibility/server-process-metrics).

![Dashboard Exampe](images/svm-dashboard-04.png)

## Review the Server Volumes Dashboard

1. Click the Volumes tab.

You can now explore the server volumes dashboard. This dashboard enables you to perform the following tasks:

- See in the list of volumes, the percentage used and total storage space available on the disk, partition or volume.
- See disk usage and I/O utilization, rate, operations per second, and wait time.
- Change the time period of the metrics collected and displayed.
- Click on any point on a chart to see the metric value for that time.

You can read more about the Server Volumes dashboard [here](https://docs.appdynamics.com/appd/23.x/latest/en/infrastructure-visibility/server-visibility/monitor-your-servers-using-server-visibility/server-volumes-metrics).

![Dashboard Example](images/svm-dashboard-05.png)

## Review the Server Network Dashboard

1. Click the Network tab.

You can now explore the server network dashboard. This dashboard enables you to perform the following tasks:

- See the MAC, IPv4, and IPv6 address for each network interface.
- See whether or not the network interface is enabled, functional, its operational state equipped with an ethernet cable that is plugged in, operating in full or half-full duplex mode, maximum transmission unit (MTU) or size (in bytes) of the largest protocol data unit that the network interface can pass, speed of the ethernet connection in Mbit/sec.
- View network throughput in kilobytes/sec and packet traffic.
- Change the time period of the metrics displayed.
- Hover over on any point on a chart to see the metric value for that time.

You can read more about the Server Network dashboard [here](https://docs.appdynamics.com/appd/23.x/latest/en/infrastructure-visibility/server-visibility/monitor-your-servers-using-server-visibility/server-network-metrics).

![Dashboard Example](https://docs.appdynamics.com/appd/23.x/latest/en/infrastructure-visibility/server-visibility/monitor-your-servers-using-server-visibility/server-network-metrics)

## Navigate between Server and Application Contexts

The Server Visibility Monitoring agent automatically associates itself with any AppDynamics APM agents running on the same host.

With Server Visibility enabled, you can access server performance metrics in the context of your applications. You can switch between server and application contexts in different ways. Follow these steps to navigate from the server main dashboard to one of the Nodes running on the server.

1. Click the Dashboard tab.
2. Click the APM Correlation link.

![Dashboard Example](images/svm-dashboard-07.png)

1. Click the down arrow on one of the listed Tiers.
2. Click the Node of the Tier.
3. Click Details.

![Dashboard Example](images/svm-dashboard-08.png)

You are now on the main Node dashboard.

1. Click the Server tab to see the related host metrics

![Dashboard Example](images/svm-dashboard-09.png)

When you have the Server Visibility Monitoring agent installed, the host metrics are always available within the context of the related Node.

You can read more about navigating between Server and Application Contexts [here](https://docs.appdynamics.com/appd/4.5.x/en/infrastructure-visibility/server-visibility/monitor-your-servers-using-server-visibility/navigating-between-server-and-application-contexts).

![Dashboard Example](images/svm-dashboard-10.png)

You have now completed this lab!


