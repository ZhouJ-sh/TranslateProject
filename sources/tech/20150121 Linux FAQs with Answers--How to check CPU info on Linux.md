Translating by ZTinoZ
Linux FAQs with Answers--How to check CPU info on Linux
================================================================================
> **Question**: I would like to know detailed information about the CPU processor of my computer. What are the available methods to check CPU information on Linux? 

Depending on your need, there are various pieces of information you may need to know about the CPU processor(s) of your computer, such as CPU vendor name, model name, clock speed, number of sockets/cores, L1/L2/L3 cache configuration, available processor capabilities (e.g., hardware virtualization, AES, MMX, SSE), and so on. In Linux, there are many command line or GUI-based tools that are used to show detailed information about your CPU hardware.

### 1. /proc/cpuinfo ###

The simpliest method is to check /proc/cpuinfo. This virtual file shows the configuration of available CPU hardware.

    $ more /proc/cpuinfo 

![](https://farm8.staticflickr.com/7572/15934711577_4136a8e0b9_c.jpg)

By inspecting this file, you can [identify][1] the number of physical processors, the number of cores per CPU, available CPU flags, and a number of other things.

### 2. cpufreq-info ###

The cpufreq-info command (which is part of **cpufrequtils** package) collects and reports CPU frequency information from the kernel/hardware. The command shows the hardware frequency that the CPU currently runs at, as well as the minimum/maximum CPU frequency allowed, CPUfreq policy/statistics, and so on. To check up on CPU #0:

    $ cpufreq-info -c 0 

![](https://farm8.staticflickr.com/7484/16094667926_d979240081_c.jpg)

### 3. cpuid ###

The cpuid command-line utility is a dedicated CPU information tool that displays verbose information about CPU hardware by using [CPUID functions][2]. Reported information includes processor type/family, CPU extensions, cache/TLB configuration, power management features, etc.

    $ cpuid 

![](https://farm9.staticflickr.com/8563/15500753923_6f1b25e8e9_c.jpg)

### 4. dmidecode ###

The dmidecode command collects detailed information about system hardware directly from DMI data of the BIOS. Reported CPU information includes CPU vendor, version, CPU flags, maximum/current clock speed, (enabled) core count, L1/L2/L3 cache configuration, and so on. 

    $ sudo dmidecode 

![](https://farm8.staticflickr.com/7503/16094667836_825b61d0e5_b.jpg)

### 5. hardinfo ###

The hardinfo is a GUI-based system information tool which can give you an easy-to-understand summary of your CPU hardware, as well as other hardware components of your system.

    $ hardinfo 

![](https://farm8.staticflickr.com/7482/15933041268_40ccc17407_b.jpg)

### 6. i7z ###

i7z is a real-time CPU reporting tool dedicated to Intel Core i3, i5 and i7 CPUs. It can display various per-core information in real time, such as Turbo Boost states, CPU frequencies, CPU power states, temperature measurements, and so on. i7z runs in either ncurses-based console mode or QT based GUI.

    $ sudo i7z 

![](https://farm8.staticflickr.com/7546/15534687744_1968dc2b18_c.jpg)

### 8. likwid-topology ###

[likwid][3] (Like I Knew What I'm Doing) is a collection of command-line tools to measure, configure and display hardware related properties. Among them is likwid-topology which shows CPU hardware (thread/cache/NUMA) topology information. It can also identify processor families (e.g., Intel Core 2, AMD Shanghai).

![](https://farm8.staticflickr.com/7511/15934711707_5dc0793599_b.jpg)

### 9. lscpu ###

The lscpu command summarizes /etc/cpuinfo content in a more user-friendly format, e.g., the number of (online/offline) CPUs, cores, sockets, NUMA nodes.

    $ lscpu 

![](https://farm8.staticflickr.com/7501/15933173470_69e53b3021_b.jpg)

### 10. lshw ###

The **lshw** command is a comprehensive hardware query tool. Unlike other tools, lshw requires root privilege because it query DMI information in system BIOS. It can report the total number of cores and enabled cores, but miss out on information such as L1/L2/L3 cache configuration. The GTK version lshw-gtk is also available.

    $ sudo lshw -class processor

![](https://farm9.staticflickr.com/8649/15498132484_a47c4e8cb3_c.jpg)

### 11. lstopo ###

The lstopo command (contained in [hwloc][4] package) visualizes the topology of the system which is composed of CPUs, cache, memory and I/O devices. This command is useful to identify the processor architecture and NUMA topology of the system.

    $ lstopo 

![](https://farm8.staticflickr.com/7490/15934399829_4012213734_z.jpg)

### 12. numactl ###

Originally developed to set the NUMA scheduling and memeory placement policy of Linux processes, the numactl command can also show information about NUMA topology of the CPU hardware from the command line.

    $ numactl --hardware 

![](https://farm8.staticflickr.com/7553/16094667876_9d7daa77a1_b.jpg)

### 13. x86info ###

x86info is a command-line tool for showing x86-based CPU information. Reported information includes CPU model, number of threads/cores, clock speed, TLB cache configuration, supported feature flags, etc.

    $ x86info --all

![](https://farm8.staticflickr.com/7522/16131238626_d8a703c060_c.jpg)

--------------------------------------------------------------------------------

via: http://ask.xmodulo.com/check-cpu-info-linux.html

译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创翻译，[Linux中国](http://linux.cn/) 荣誉推出

[1]:http://xmodulo.com/how-to-find-number-of-cpu-cores-on.html
[2]:http://en.wikipedia.org/wiki/CPUID
[3]:http://xmodulo.com/identify-cpu-processor-architecture-linux.html
[4]:http://xmodulo.com/identify-cpu-processor-architecture-linux.html
