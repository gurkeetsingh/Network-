# Virtualization

- creating a logical representation of a component through software. also known as a virtual component
- a virtual machine is a software based computer
- example are: virtual machine, virtual network adapters, virtual network devices

## host machine

- a virtualized machine is created on a physical computer known as a `host machine`. it is a physical machine `hosting` virtual components
- it provides computing resources to the guest

## virtual machine

- it is also known as a `guest` as they are the guest on the host means using its resources

## hypervisor

- there are 2 types of hypervisor
- type 1 hypervisor are: `bare metal hypervisor` as there is no operating system running on the machine, it is the hypervisor itself that is allowing us access to the hardware. so the bottom layer is the hardware, then comes the hypervisor and on the top of hypervisor we install the virtual machine. the hypervisor `abstract` all the hardware from the virtual machine software. this a scalabel `hypervisor` as long as we got the resources 
- type 2 hypervisor: in this type the bottom layer is hardware layer which is the same then comes the operating system on which we install the `virtual application` running side by side with other application within operating system on which we can install the virtual machine. for example `virtualbox`. in this the hypervisor talks to the operating system for the resources it needs and then operating system access the hardware resources for that virtual application 

## Virtual network adapters

## network function virtualization

## Virtual networking software

- Virtual networking software is used to create virtual networking components. These components are used to connect physical or virtual devices. Virtual networking software can simulate physical devices and also functions the same. The only difference is that software is used for these devices.