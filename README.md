# Project Description

I developed the core of an operating system, including the boot stage setup, paging machenisim, PIC interface between hardware devices and OS software, in-memory file system and disk file system implementation, system call interface between user programs and OS as well as scheduler and multiple terminal. (See the full feature list below)

## Basic features

- [x] GDT, LDT, TSS initialized, use GRUB to boot the OS image file
- [x] enable 4KB user pages (video memory and program stacks) and 4MB OS page
- [x] PIC initialized to enable keyboard, mouse, sound drive, RTC, PIT etc. 
- [x] IDT initialized and the items associated those devices are filled
- [x] Memory buffer operations (open, read, write, close) implemented after reading file data from harddisk driver
- [x] System call linkage (in Assembly) and interface between user programs and OS services
- [x] PCB created, support user program execution 
- [x] Scheduler and task switching, multiple terminal implemented (with virtually separate keyboard buffer, video memory, cursor, etc. One program executes without noticing the execution of other programs)

## Advanced features

- [x] Add more hardware features such as PS2 mouse, sound drive.

- [x] Writable fs
  
  - [x] Implemented hard disk driver to support reading chunks of data from the hard disk and writing chunks of data into the hard disk
  
  - [x] Implemented The Second Extended File System (EXT2) parser to support `read`, `open`, `close`, `write` and `delete` file operations

- [x] GUI
  
  - [x] Implemented VBE & VGA hardware drivers
  
  - [x] Able to load and display images stored in the hard disk as a file.

  - [x] Able to draw icons, buttons on the screen to support mouse click
  
  - [x] Able to display graphical text on the screen
    
  - [x] Graphical Shell
  
  - [x] Display status bar at the bottom of the screen and create application windows (for example, multiple overlapping terminal windows which can be dragged by mouse)

- [x] Buddy allocation system
  
  - [x] Implemented buddy allocation algorithm similar to the real Linux operating system
  
  - [x] Able to allocate reasonable amount of free memory space to the user programs when there's a request (system call) from user programs

