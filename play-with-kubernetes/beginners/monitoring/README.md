# Kubernetes Monitoring

## Modernation Journey

If you go back around 4-5 years go and look at some past example, the tools which we use in the past is not going to work today.When we think of monitoring solution, there is a type of instrumentation which takes place and get displayed
Bare Metal Server was very straighforward. Tools like Nagios, Ganglia, Zabbix etc shows CPU, Memory

When we split it out to VMs, Virtualized version of bare metal system, some kind of monitoring agent inside VMs, that typically worked because each of
of these VMs hve isolated machine, kernel

Now its world of container, idea of isoltion is broken, If we tried to instrument each of the monitoring agent, I would end up commiting sins which is 
something has nothing to do with these containers.

Recommendation #1: We Don't put monitoring code inside Docker Container.


Arises a basic question - In a containerization world, if you are not inside container, how are you going to monitor?
Containers are black boxes to legacy tooling How do I see performance and metrics inside



New Technology - Containers are black boxes to legacy tooling - How do I see performance & activity inside?
New Architecture - Dyanamic Microservices are compelex to monitor - How to do I monitor and alert on distributed services?
New Processes - Identifying bottlenecks & root cause - How do I troubleshoot ephimeral containers?

