# SRE Interview Prep

I've been in management for too long, and I wanted to remember why it was I actually liked working
with Linux in the first place, so I'm keeping this list of interesting things that I may want to
review before I interview next and some random notes.

Honestly, this is just a list of interesting things I come across and think could be useful someday.
I'm not really sure why I named it interview prep other than that I got the idea to save it from looking
at a couple of SRE interview prep repos.

## Linux Internals

### VM Subsystem

* [Video: The Future of the Linux Page Cache, Matthew Wilcox](https://www.youtube.com/watch?v=xxWaa-lPR-8)
* [Video: MM 101 - Introduction to Memory Management, Christoph Lameter](https://www.youtube.com/watch?v=i17b3xJv3Uo)
* [PDF: Linux Memory Management, Kaustubh R. Joshi](http://www.cs.columbia.edu/~krj/os/lectures/L17-LinuxPaging.pdf)


### ELF, shared libraries, etc.

* [LWN: How programs get run; ELF binaries](https://lwn.net/Articles/631631/)
* [Eli Bendersky: Load-time relocation of shared libraries](https://eli.thegreenplace.net/2011/08/25/load-time-relocation-of-shared-libraries/)

### System Calls

* [Packagecloud: The Definitive Guide to Linux System Calls](https://blog.packagecloud.io/eng/2016/04/05/the-definitive-guide-to-linux-system-calls/)
* [MD: Linux Insides, System Calls, 0xAX](https://github.com/0xAX/linux-insides/tree/master/SysCall)

### I/O

* [Linux Block IO: Introducing Multi-queue SSD Access onMulti-core Systems, Matias Bjørling, Jens Axboe, David Nellans, Philippe Bonnet](http://kernel.dk/systor13-final18.pdf)


## Interesting Linux Interview Questions

There's a dearth of decent questions out there to ask candidates or to think about when prepping for an
interview. Lots of the ones that are out there are either stupid and meaningless ("what's the best linux
distro"), outdated ("what's LILO") or are ambiguous enough that there aren't any right answers ("what's
the first thing you must do with a new Linux system"), so here are some fun questions I've asked or been
asked, some classics, some just interesting.

### General interest

* How many ways can you think of to delete a file named "-f"?
* How many ways can you think of to fix a system where something has removed the executable bits on /usr/bin/chmod binary's permissions?

### Kernel stuff

* The program you're `strace`-ing  is doing nothing but `brk()/sbrk()` and `mmap()/munmap()` system calls. What's the most likely
  explanation for what it's doing under the hood?
* Explain in as much detail as possible what happens once you type `ls -l /` into your shell and hit enter.
