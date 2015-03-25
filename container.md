## Linux container

The concept container in linux refers to isolated light weight OS environment for running processes. A container appears as a complete OS (with root filesystem, network, hostname) dedicated to a process. 

Comparing to virtual machine, Linux container (including lxc, docker, rocket) provides reasonable good isolated environment at much cheaper cost (in term time and resource).

The linux kernel provide a set of syscall(s) that is utilized by container's tools to create and manage of containers.

These syscal are of two groups

* namespace: which prevent collision in using named resources e.g. process id, ipc, network port, filesystem, hostname
* cgroups: allocate physical resources (cpu, memory, io) to each container

**docker**

References

* http://blog.dotcloud.com/under-the-hood-linux-kernels-on-dotcloud-part
* http://blog.dotcloud.com/kernel-secrets-from-the-paas-garage-part-24-c