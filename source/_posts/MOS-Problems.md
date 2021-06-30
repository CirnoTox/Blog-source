---
title: MOS_Problems
date: 2021-06-03 20:43:46
tags: Operating_System
---

Following answers are for reference only.

# Introduction
1. What are the two main functions of an operating system?
   
   1. Provding user programs with a better, simpler, cleaner model of the computer.
   2. Handling managment of all the resources.
2. In Section 1.4, nine different types of operating systems are described. Give a list of
applications for each of these systems (one per operating systems type).

    | Type of OS | Aplications |
    |-|-|
    | Mainframes | It makes something of a comeback as high-end Web servers, servers for large-scale electronic commerce sites, and servers for business-to-business transactions. |
    | Server | It serve multiple users at once over a network and allow the users to share hardware and software resources.It can provide print service, file service, or Web service.  |
    | Multiprocessors | It provides a major-league computing power, which makes conventional desktop and notebook operating systems are starting to deal with at least small-scale multiprocessors.  |
    | PC | Their job is to provide good support to a single user. They are widely used for word processing, spreadsheets, games, and Internet access. With modern CPU, it is gradually changing into the Multiprocessors OS.  |
    | Handheld computer | Smartphones and tablets. |
    | Embedded | It do not accept user-installed software.Wifi routers,Microwave ovens, DVD recorders.|
    | Sensor-node | Sensor networks are used to protect the perimeters of buildings, guard national borders, detect fires in forests, measure temperature and precipitation for weather forecasting, glean information about enemy movements on battlefields, and much more. |
    | Real-time | On industrial process-control systems, real-time computers have to collect data about the production process and use it to control machines in the factory. |
    | Smart Card | electronic payments|

3. What is the difference between timesharing and multiprogramming systems?
   
    
    Timesharing is a kind of service offered by Mainframe OS.It is also a variant of multiprogramming,it allow s multiple remote users to run jobs on the computer at once, such as querying a big database. 
    
    Timesharing faces to users but multiprogramming faces to programs.Multiprogramming need a context switch, Timesharing not.
    
4. To use cache memory, main memory is divided into cache lines, typically 32 or 64 bytes long. An entire cache line is cached at once. What is the advantage of caching an entire line instead of a single byte or word at a time.
   
   Cache hits normally take about two clock cycles.If caching a single byte or word at a time is used, more time will be spent.

5. On early computers, every byte of data read or written was handled by the CPU (i.e., there was no DMA). What implications does this have for multiprogramming?

    The CPU allowed multiple programs to run however they had to all run in sequence (there was no DMA) which could cause the programs to become backed up since they would have to wait for one process to end before another one could be initiated.

6. Instructions related to accessing I/O devices are typically privileged instructions, that is, they can be executed in kernel mode but not in user mode. Give a reason why these instructions are privileged.

    It is up to the operating system to manage the system security so that files, for example, are accessible only to authorized users. Files in UNIX are protected by assigning each one a 9-bit binary protection code.

7. The family-of-computers idea was introduced in the 1960s with the IBM System/360 mainframes. Is this idea now dead as a doornail or does it live on?

    It still lives on. A good expamle is the Mac.


8. One reason GUIs were initially slow to be adopted was the cost of the hardware needed to support them. How much video RAM is needed to support a 25-line × 80-row character monochrome text screen? How much for a 1200 × 900-pixel 24-bit color bitmap? What was the cost of this RAM at 1980 prices ($5/KB)? How much is it now?

    A 25x80 character monochrome text screen requires a 2000-byte buffer. The 1024x768 pixel 24-bit color bitmap requires (1024*768*24/8) 2,359,296 bytes. In 1980 these two options would have cost $10 and $11,520, respectively. For current prices, check on how much RAM currently costs, probably less than $1/MB.Gloway 4GB is 125 yuan, so 1byte is (125/4/1024/1024)yuan.

9. There are several design goals in building an operating system, for example, resource utilization, timeliness, robustness, and so on. Give an example of two design goals that may contradict one another.

    An OS supported the multithread may have less robustness.(?)

10. What is the difference between kernel and user mode? Explain how having two distinct modes aids in designing an operating system.

    In kernel mode, there is access of hardware resource. In user mode, a TRAP is needed to change into kernel mode to get access of hardwawre resource.These two modes ensure the safty of hardware resource.Instead of your entire system crashing, only that particular application crashes. That's the value of User mode.

11. A 255-GB disk has 65,536 cylinders with 255 sectors per track and 512 bytes per sector. How many platters and heads does this disk have? Assuming an average cylinder seek time of 11 ms, average rotational delay of 7 msec and reading rate of 100 MB/sec, calculate the average time it will take to read 400 KB from one sector.
    
    