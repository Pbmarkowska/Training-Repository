[Source: Medium](https://medium.freecodecamp.org/a-beginner-friendly-introduction-to-containers-vms-and-docker-79a9e3e119b)

Used for packing, shipping and running applications within containters.

### VM vs Docker
VM (Virtual Machine) - emulation of a real computer that executes programs like a real computer.

VM run on top of a physical machine using 'hypervisor'. 'Hypervisor' is a piece of software, firmware, or hardware that VMs run on top of.

A hypervisor, in turn, runs on either a 'host machine' or on 'bare-metal'.

Host machine provides the VMs with resources, including RAM and CPU.

A VM that is running on the host machine (again, using hypervisor) is also often called a 'guest machine'. 'Guest machine' can run on either a hosted hypervisor or a bare-metal hyperviso

This 'guest machine' contains both the application and whateer it needs to run that application (e.g. system binaries and libraries). It also carries an entire virtualized hardware stack of its own, including virtualized network adapters, storage, and CPU - which means it also has its own full-fledged guest operating system.

Differences between hosted hypervisor and bare-metal hypervisor:

#### Hosted Hypervisor

 - runs on the operating system of the host machine
 - doesn't have direct access to the hardware, so it has to go through the host operating system
 - The benefit of a hosted hypervisor is that the underlying hardware is less important.
 - The host's operating system is responsible for the hardware drivers instead of the hypervisor itself.

#### Bare-Metal Hypervisor

- installs and runs from the host machine's hardware, it interfaces directly with the underlying hardware it doesn't need a host operating system to run on
 - has its own device drivers and interacts with each component directly for any I/O, processing or OS-specific tasks.
 - Unlike VM, which provides hardware virtualization, a container provides operating-system-level virtualization by abstracting the 'user space'

#### VM and container similarities:

 - they have private space for processing
 - they can execute commands as root
 - they have a private interface and IP address
 - they allow custom routes and iptable rules
 - they can mount file systems etc.
 - The one big difference between containers and VMs is that containers share the host system's kernel with other containers.