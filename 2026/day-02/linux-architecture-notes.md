#Linux System Fundamentals

		Welcome to the Linux System Fundamentals Guide.
		This document explains Linux architecture, the boot process, file system structure, and essential commands for daily system operations.

#1. Linux Architecture

		The Linux operating system is designed in layers to allow smooth communication between users and hardware.
		
		Main Layers
		
		Hardware
		Physical components such as CPU, RAM, hard disk, and motherboard.
		
		Kernel
		The core of Linux. It manages hardware, memory, processes, and system resources.
		
		Shell
		A command-line interface that accepts user commands and passes them to the kernel.
		
		Applications / Users
		Software programs and human users who interact with the system.
		
		Key Concept

High-level programs (written in C, Python, etc.) are converted into machine-readable binary code (0s and 1s) so the hardware can execute them.

#2. Linux Boot Process

		The boot process is the sequence of steps that starts the Linux system.
		
		Boot Steps
		
		Power On
		System receives power.
		
		BIOS / UEFI
		Initialises hardware and performs Power-On Self-Test (POST).
		
		GNU GRUB (Bootloader)
		Loads the Linux kernel into memory.
		
		Kernel Loading
		Kernel initializes hardware drivers and system memory.
		
		Systemd / Init (PID 1)
		Starts system services and background processes.
		
		Login Screen
		User is presented with a login prompt.

#3. File System Hierarchy

	Linux uses a tree structure that starts from the root directory /.

#Important Directories
		Directory	Description
		/	Root directory (starting point)
		/home	User home directories
		/root	Home directory of root user
		/boot	Bootloader and kernel files
		/etc	Configuration files
		/bin	Essential user commands
		/sbin	System administration commands
		/usr	User programs and applications
		/var	Variable data (logs, cache)
		/dev	Device files
		/opt	Optional software
		/tmp	Temporary files
		/lib	Shared libraries
		/media	Mount point for removable devices
		/proc	Virtual filesystem (process info)

#4. Essential Linux Commands
	A. Navigation & File Management
		Task	Command	Example
		Change directory	cd	cd /home/user
		Create folder	mkdir	mkdir docs
		Create file	touch	touch file.txt
		Copy file	cp	cp a.txt b.txt
		Move/Rename	mv	mv a.txt new.txt
		Delete file	rm	rm file.txt
		Delete folder	rm -r	rm -r myfolder

 Warning: rm -r permanently deletes folders. Use carefully.

##B. Network Commands
		Task	Command	Example
		Show IP address	ip addr	ip addr show
		Check connectivity	ping	ping google.com
		
	    Stop ping with: Ctrl + C

##C. System Monitoring
		Task	Command	Description
		Disk usage	df -h	Shows storage in GB/MB
		RAM usage	free -h	Shows memory usage
		CPU & processes	top	Live system monitor
		Better monitor	htop	Advanced monitor (if installed)
#5. Useful Additional Commands (For DevOps & Admins)
		Task	Command
		Show running processes	ps aux
		Check system uptime	uptime
		Check disk usage per folder	du -sh *
		Check OS version	uname -a
		View logs	journalctl
		Switch user	su
		Run as admin	sudo
