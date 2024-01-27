---
tags: fc, os
course: Operating Systems
---

# Introduction

A program that acts as an intermediary between a user of a computer and the computer hardware ;; Operating System

Operating System goals 
,,
- Execute user programs and make solving user problems easier
- Make the computer system convenient to use
- Use the computer hardware in an efficient manner

# Four componenets of a computer system 

provides basic computing resources ;; Hardware 

controls and coordinates use of hardware among various applications and users ;; Operating system 

define the ways in which the system resources are used to solve the compouting prolems of the users ;; Application programs 


People, machines, other computers are exampels of ;; Users


# What Operating Systems Do 

Depends on the ==point of view==

Users want convenience, ==ease of use==, Don't care about ==resource utilization==

But shared computer such as ==mainframe== or ==minicomputer== must keep all users happy 

Users of dedicate systems such as ==workstations== have dedicated resourcesa but frequently use shared resouces from ==servers==.

Handheld computers are ==resource poor==, optimized for ==usability== and ==battery life==

Some computer have little or no ==user interface==, such as embedded computers in devices and automobiles

# Operating System Definition 
OS is a **resource allocator**
,, 
- Manages all resrouces 
- Decides between conflicting requests fro efficient and fair resource use 

OS is a **control program** 
,,
- Controls execution of programs to prevent errors and improper use of the computer 

Operating system has no universally accepted definition ;; True 


"Everything a vendor ships when you order an operating system" is ==good approximation==, but varies wildly 

"The one program running at all times on the computer" is the ==kernel==. Everything else is either a system program (ships with the operating system) or an application program.

==bootstrap program== is loaded at power-up or reboot 
,,
- Typically stored in ROM or EPROM, generally known as ==firmware==
- Initiates all aspects of system 
- Loads operating system kernel and starts execution 

Computer-system operation 
,, 
- One or more CPUs, device controllers connect through common bus providing access to shared memory
- concurrent execution of CPUs and devices competing for memory cycles 


# Computer-System Operation 

I/O devices and the CPU can ==execute concurrently==

Each device controller is in charge of a particular ==device type==

Each device controller has a ==local buffer== 

CPU moves data from/to ==main memory=== to/from ==local buffers==

I/O is from the device to ==local buffer== of ==controller==

Device controller informs CPU that it as finished its operation by causing an ==interupt==

# Common Functions of Interrupts

Interrupt transfers control to the interrupt service routine generally, through the ==interrupt vector==, which contains the addresses of all the service routines

==Interrupt architecture== must save the address of the ==interrupted instruction==

A ==trap== or ==exception== is a software-generated interrupt caused either by an error or a user request

An operating system is ==interrupt driven==

# Interrupt Handling 

The operating system preserves the state of the CPU by ==storing registers== and the ==program counter==

Determines which type of interrupt has occured: 
,,
- Polling 
- vectored interrupt system 

==Separate segments of code== determine what action should be taken for each type of interrupt


After I/O starts, control returns to user program only upon I/O completion 
,,
- Wait instruction idles the CPU until the next interrupt
- Wait loop (contention for memory access) ! At most one I/O request is outstanding at a time, no simultaneous I/O processing


request to the OS to allow user to wait for I/O completion ;; System call 

contains entry for each I/O decice indicating its type, address, and state ;; Device-status table

==OS indexes== into I/O device table to determine device status and to modify table entry to include interrupt


# Direct Memory Access Structure

Used for ==high-speed I/O devices== able to transmit information at close to memory speeds

transfers blocks of data from buffer storage directly to main memory without CPU intervention ;; Device controller 

Only one interrupt is generated per block, rather than the one interrupt per ==byte==

# Storage Structure 

only large storage media that the CPU can access directly ;; Main Memory

extension of main memory that provides large nonvolatile storage capacity ;; Secondary storage

rigid metal or glass platters covered with magnetic recording material ;; Magnetic disks 

Disk surface is logically divided into ==tracks==, which are subdivided into ==sectors==

determines the logical interaction between the device and the computer ;; The disk controller

faster than magnetic disks, nonvolatile ;; Solid-state disks


Storage systems organized in hierarchy
,,
- Speed
- Cost 
- Volatility 

copying information into faster storage system; main memory can be viewed as a cache for secondary storage ;; Caching 

for each device controller to manage I/O. Provides uniform interface between controller and kernel ;; Device driver 

# Computer-System Architecture 

Most systems use a ==single general-purpose processor== (PDAs through mainframes)

Multiprocessors 
,,
- systems growing in use and importance 
- Also known as parallel systems, tightly-coupled systems 
- Advantages include: 
	- Increased thoughput 
	- Eceonmy of scale 
	- increased Reliability

## Two types of multiprocessors 

a processor is assigned a specific task ;; Asymmetric Multiprocessing

each processor performs all tasks within the OS. ;; Symmetric Multiprocessing


# Clustered Systems 

Clustered systems usually shares storage via a ==storage-area network (SAN)==

has one machine in hot-standby mode ;; Asymmetric clustering 

has multiple nodes running applications, monitoring each other ;; Symmetric clustering 

# Operating System structure

**Multiprogramming** need for effiency
,,
- Single user cannot keep CPU and I/O devices busy at all times 
- Multiprogramming organizes jobs (code and data) so CPU always has one to execute 
- A subset of total jobs in system is kept in memory 
- One job selected and run via job scheduling 
- When it has to wait (for I/O for example), OS switches to another job


 is logical extension in which CPU switches jobs so frequently that users can interact with each job while it is running, creating interactive computing ;; TimeSharing (multitasking)


# Operating-System Operations 

Software error or request creates ==exception== or ==trap== (ex. Dividing by 0)

operation allows OS to protect itself and other system components ;; Dual-mode

Examples of dual mode:
,,
- User mode and kernel mode

Exmaple of Dual mode is ==Mode bit== that provides abilitty to distinguish when system is running user code or kernel code 

# Transition from User to kerel Mode 
Timer to prevent infinite loop / process hogging resources 
,,
- Set interrupt after specific period 
- Operating system decrements counter 
- When counter zero generate an interrupt 
- Set up before scheduling process to regain control or terminate program that exceeds allotted time

# Process management 

A process is a program in execution. It is a unit of work within the system. Program is a ==passive entity==, process is an ==active entity==.

Process needs resources to accomplish its task
,,
- CPU, memory, I/O, files 
- Initialization data 

==Process termination== requires reclaim of any reusable resources

Single-threaded process has one ==program counter== specifying location of next instruction to execute

has one program counter per thread ;; Multi-threaded process


# Process management activities 

The operating system is responsible for the following activities in connection with process management:
,,
- Creating and deleting both user and system processes 
- Suspending and resuming processes 
- Providing mechanisms for process synchronization 
- Providing mechanisms for process communication 
- Providing mechanisms for deadlock handling 


# Main memory 

==Main memory== is central to the operation of a modern computer system

All ==instructions== in memory in order to execute

Memory management determines what is in memory when ==Optimizing CPU== utilization and computer response to users

Memory management activities
,, 
- Keeping track of which parts of memory are currently being used and by whom 
- Deciding which processes (or parts thereof) and data to move into and out of memory 
- Allocating and deallocating memory space as needed

# Storage management

Abstracts physical properties to logical storage unit ;; file 


Files usually organized into directories. Access control on most systems to determine who can access what ;; File-System Management

OS activities 
,, 
- Creating and deleting files and directories 
- Primitives to manipulate files and dirs 
- Mapping files onto secondary storage 
- Backup files onto stable (non-volatile) storage media


# Mass-Storage Management

Usually disks used to store data that does not fit in ==main memory== or ==data== that must be kept for a “long” period of time

Proper management is of ==central importance==


OS activities 
,,
- Free-space management 
- Storage allocation 
- Disk scheduling

includes optical storage, magnetic tape ;; Tertiary storage 

# I/O Subsystem 

One purpose of ==OS== is to hide details of hardware devices from the user


Responsibility of an I/O subsystem  where storing data temporarily while it is being transferred ;; buffering 

Responsibility of an I/O subsystem where storing parts of data in faster storage for performance ;; Caching 

Responsibility of an I/O subsystem where the overlapping of output of one job with input of other jobs ;; Spooling 

# Protection and Security

any mechanism for controlling access of processes or users to resources defined by the OS ;; Protection 

defense of the system against internal and external attacks ;; Security


include name and associated number, one per user ;; User identities 

allows set of users to be defined and controls managed, then also associated with each process, file ;; Group identifier

allows user to change to effective ID with more rights ;; Privilage escalation 

# Computing Environments - Traditional 

provide web access to internal systems ;; Portals

==Network computers (thin clients)== are like Web terminals

Mobile computers interconnect via ==wireless networks==

Networking becoming ubiquitous – even home systems use ==firewalls== to protect home computers from Internet attacks


# Computing Environments - Distributed 

Collection of separate, possibly heterogeneous, systems networked together ;; Distributed 


is a communications path, TCP/IP most common ;; Network

provides features between systems across network. Communication scheme allows systems to exchange messages. llusion of a single system ;; Network Operating System 

# Computing Environments - Client-Server 

Dumb terminals supplanted by smart PCs ;; Client-Server Computing 

Many systems now ==servers==, responding to requests generated by ==clients==

provides an interface to client to request services (i.e., database) ;; Compute-server system

provides interface for clients to store and retrieve files ;; File-server system 

# Computing Environments - Peer-to-Peer

Instead all nodes are considered peers  that may each act as client, server or both ;; Peer to Peer Computing Environment 

Node must join P2P network 
,,
- Registers its service with central lookup service on network, or
- Broadcast request for service and respond to requests for service via discovery protocol


# Computing Environments - Virtualization

Allows operating systems to run applications within other OSes ;; Virtualization 

used when source CPU type different from target type (i.e. PowerPC to Intel x86) ;; Emulation

When computer language not compiled to native code ;; Interpretation 


OS natively compiled for CPU, running guest OSes also natively compiled ;; Virtualization 

Consider VMware running WinXP guests, each running applications, all on native WinXP ==host== OS

provides virtualization services ;; VMM

# Computing Environments – Cloud Computing

Delivers computing, storage, even apps as a service across a network ;; Cloud Computing 

Amazon ==EC2== has thousands of servers, millions of VMs, PBs of storage available across the Internet, pay based on usage

available via Internet to anyone willing to pay ;; Public cloud 

run by a company for the company’s own use ;; Private cloud 

includes both public and private cloud components ;; Hybrid Cloud

one or more applications available via the Internet (i.e. word processor) ;; Software as a service 

software stack ready for application use via the Internet (i.e a database server) ;; Platform as a service 

servers or storage available over Internet (i.e. storage available for backup use) ;; Infrastructure as a service

==Cloud compute environments== composed of traditional OSes, plus VMMs, plus cloud management tools

# Computing Environmnets - Real-Time Embedded Systems 


Real-time embedded systems most prevalent form of computers 
,, 
- Vary considerable, special purpose, limited purpose OS, real-time OS 
- Use expanding

Some have OSes, some perform tasks without an ==OS==


Real-time ==OS== has well-defined fixed time constraints.  Processing must be done within constraint. Correct operation only if ==constraints== met

# Open-Source Operating Systems

Operating systems made available in source-code format rather than just binary ==closed-source==

! Counter to the copy protection and ==Digital Rights Management== (DRM) movement

Started by ==Free Software Foundation== (FSF), which has “copyleft” ==GNU== Public License (GPL)