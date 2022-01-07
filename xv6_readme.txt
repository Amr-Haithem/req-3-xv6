In this project, We introduce a 2-level paging mechanism and page replacement policies to xv6 operating system.

There are 2 paging policies: FIFO and LRU.

These policies are invoked with the SELECTION flag when launching, i.e.

$sudo make clean qemu-nox SELECTION=FIFO

If the flag isn't defined at launch, then FIFO is used.

--------------------------------------------------------------------

BUILDING AND RUNNING XV6

To build and run xv6 on windows:
- install WSL (windows subsystem for linux) - UBUNTU.
- install the QEMU emulator and xv6 through following commands in UBUNTU shell:

1) sudo apt-get update
2) sudo apt-get install build-essential
3) Sudo apt-get install gcc-multilib
4) sudo apt install qemu qemu-utils qemu-kvm virt-managerlibvirt-daemon-system libvirt-clients bridge-utils
5) sudo apt-get install git-core
6) sudo git clone git:https://github.com/Amr-Haithem/xv6-project.git
7) cd xv6-project
8) sudo make
9) sudo make qemu-nox


To build xv6 on an x86 ELF machine (like Linux or FreeBSD), run "make".
On non-x86 or non-ELF machines (like OS X, even on x86), you will
need to install a cross-compiler gcc suite capable of producing x86 ELF
binaries.  See http://pdos.csail.mit.edu/6.828/2014/tools.html.
Then run "make TOOLPREFIX=i386-jos-elf-".

