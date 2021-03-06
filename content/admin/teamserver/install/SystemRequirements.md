<!--
  title: "System Requirements",
  description: "Minimum system requirements for running the EOP TeamServer",
  tags: "EOP requirements installation sizing libraries libaio"
-->

## Preparing for the Installation
The Contrast Enterprise on Premise (EOP) TeamServer includes a Tomcat servlet container, a MySQL database instance and an Oracle Hotspot Java Virtual Machine. All of these components are embedded within the installation binary and deployed to a single server as part of the TeamServer architecture. Very little preparation is needed by customers to perform an installation of the TeamServer. Customers should prepare the following prior to installing:

* System with adequate compute and memory resources based on guidance from our sizing recommendations
* Adherence to the system requirements specified below
* Installation of the MySQL run-time libraries (Linux Only)

## System Requirements

| Category            | Minimum   | Recommended | Description |
| :------------------ | :-------- | :---------- | :---------- |
| **OS Architecture** | 64-bit | 64-bit | Due to memory requirements, TeamServer will **only** run on 64-bit architectures. |
| **Operating System** | <ul><li>Microsoft Windows 2008 R2 64-bit</li> <li>Ubuntu 12.04 LTS</li><li>Centos 6</li></ul> | <ul><li>Microsoft Windows 2012 R2  </li><li>  Ubuntu 14.04 LTS </li><li> Centos 7</li></ul>| Any modern Operating System **should** run Contrast - we officially support the following: <ul><li>Ubuntu Linux </li><li> Debian Linux </li><li> Redhat Enterprise Linux </li><li> Centos Linux </li><li> Windows Server 2008 R2 64-bit </li><li> Windows 2012 R2 </li> |
| **Java | 1.7.0_80  | 1.7.0_80 or greater |
| **MySQL | 5.6.28 | 5.6.33 |

## MySQL Shared Libraries
Customers running TeamServer will need to pre-configure their base operating system on Linux with a shared library for running MySQL. Depending on which flavor of Linux deployed with TeamServer, follow the installation options below:

**Customers Running Centos or RHL**
````
[contrast@myserver ~]# yum install libaio 
````

**Customers Running Ubuntu or Debian**
````
[contrast@myserver ~]# apt-get install libaio1 libaio-dev
````

