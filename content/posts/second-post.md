---
title: "What Is Container(ization)?"
date: 2022-11-28T15:53:42+05:30
draft: false
---

Containerization is a process of packaging your application together with its dependencies into one package (a container). Such a package can then be run pretty much anywhere, no matter if it’s an on-premises server, a virtual machine in the cloud, or a developer’s laptop. By abstracting the infrastructure, containerization allows you to make your application truly portable and flexible.

Before we dive into explaining containers in the context of DevOps, let’s first talk about containers themselves.

Problems of Traditional Applications
Traditionally, to install and run any software on any server, you need to meet several requirements. The software needs to support your operating system, and you probably need to have a few libraries and tools installed to run the software. But that’s not all.

All these requirements probably need to be in a specific version and accessible at the specific path. Also, sometimes you may need to have proper permissions for certain directories and files. Overall, there are quite a few checkboxes you need to tick before you can successfully run the software.

These requirements create certain problems. First, what if you already have some of the tools or libraries installed, but in an unsupported version? You’d have to upgrade or downgrade them, hoping it won’t break any existing software. The problems don’t end once requirements are met and the application is running correctly, though.

What if you want to run the application in another cloud environment? You’ll have to start the process all over again. Containers are meant to solve these problems.

Containers to the Rescue
The idea of a container is to package these libraries, tools, and any other things your application requires into one “executable package”—a container. Then you can run these containers without worrying about the libraries because everything is already included in a container.  Containers isolate software from the cloud environment and make sure it works the same way regardless of potential environmental differences.   

Containers vs. Virtual Machines
This all might sound like a concept of a virtual machine deployed from a prebuilt image, but containers work much differently. The main difference between a VM and a container is a container virtualizes the operating system, whereas a virtual machine is an abstraction of physical hardware. This difference results in containers being more efficient and portable than VMs.

So, how do containers achieve isolation and portability? In the case of a Linux system, the answer is cgroups and namespace isolation. You can run containers on Windows, too. The Windows kernel uses different mechanisms to achieve the same results. Instead of cgroups it has job objects, and instead of namespaces it has server silo objects. These features of Windows and Linux kernels allow building containers, which encapsulate everything your application may need without creating any conflicts with the host operating system and other containers.

Because they achieve the same functionality as VMs (isolation, ability to package all you need into one executable piece), some people call containers “lightweight VMs.” “Lightweight” comes from the fact that whereas a VM includes a full copy of an operating system, the application, and binaries and libraries that can take up space and be slow to boot. Containers share the operating systems and infrastructure with other containers, with each container running as isolated processes in user space. Since containers are fundamentally different than virtual machines in how they’re constructed, it’s best to avoid calling them “lightweight VMs.” 