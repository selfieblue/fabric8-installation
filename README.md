# fabric8-installation

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/io.fabric8/fabric8-maven-plugin/badge.svg?style=flat)](https://maven-badges.herokuapp.com/maven-central/io.fabric8/fabric8-maven-plugin/)

<p align="center">
  <a href="http://fabric8.io/">
  	<img src="https://raw.githubusercontent.com/fabric8io/fabric8/master/docs/images/cover/cover_small.png" alt="fabric8 logo"/>
  </a>
</p>

### Server Specifications
+ k8s controlplane : CPU 2 Cores, Ram 4 GB, Disk 20 GB
+ k8s minion x2    : CPU 4 Cores, Ram 8 GB, Disk 50 GB
+ nfs              : CPU 1 Cores, Ram 2 GB, Disk 50 GB


### Introduction
These scripts has bee provide to get started fabric8 on centos 7 and this poc need nfs server to be fabric8 storage:
+ Firstly, provision the nfs and configure path that you can found in the 1-nfs-server-installation.txt
+ Secondly, install kubernetes version 1.9.7 and build k8s cluster included install calio network plugin
* Thirdly, after k8s cluster is up and running, you need to create pv and pvc base on mountpoint on nfs server
* Lastly, install fabric8, in this case I use my macbook to install fabric8