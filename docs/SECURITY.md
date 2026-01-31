# Security - NanoKVM

## Infrastructure setup

* Fully automated with ansible
* Upstream ansible role with continuous integration and weekly test.

## Mitigating factors

### Identity

* SSH access with ssh-key only. Add those from Web UI initially.

### System

* (option?) disable default route
* configure specific dns nameservers that could be used with allow/block lists

### Network

Ensure to cover both IPv4 and IPv6.

|From|To|protocol/port|
|----|--|-------------|
|System|selected DNS servers|tcp+udp/53|
|System|NTP server|udp/123|
|Private Networks|System|tcp/22|
|System|cdn.sipeed.com (optional, for system updates from Internet)|tcp/443|
|System|Website (optional)|tcp/443|
