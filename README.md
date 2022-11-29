# Project Description

I developed the core of an operating system (OS), including the boot stage setup, paging machenisim, PIC interface between hardware devices and OS software, in-memory file system and disk file system implementation, system call interface between user programs and OS as well as scheduler and multiple terminal. (See the full feature list below)

## Basic features

- [x] Global Descriptor Table (GDT), Local Descriptor Table (LDT), Task State Segment (TSS) initialized, use GRUB to boot the OS image file.
 
- [x] Enable 4KB user pages (video memory and program stacks) and 4MB OS page.

- [x] Programmable Interrupt Controller (PIC) initialized to enable keyboard, mouse, sound drive, Real-Time Clock (RTC), Periodic Interrupt Timer (PIT), etc. 
 
- [x] Interrupt Descriptor Table (IDT) initialized and the items associated with those hardware devices are filled.
 
- [x] Memory buffer operations (open, read, write, close) implemented after reading file data from the in-memory file system.
 
- [x] Implemented System call linkage (in Assembly) to provide OS services to the user programs.
 
- [x] Implemented Process Control Block (PCB) to support the execution of user programs.
 
- [x] Implemented scheduler to support task switching.

- [x] Supported multiple terminals with virtually separate keyboard buffer, video memory, cursor, etc. Such that one program can execute without noticing the execution of other programs.

## Advanced features

- [x] Suuported more hardware devices such as PS2 mouse, sound drive,etc.

- [x] Writable File System
  
  - [x] Implemented hard disk driver to support reading chunks of data from the hard disk and writing chunks of data into the hard disk
  
  - [x] Implemented The Second Extended File System (EXT2) parser to support `read`, `open`, `close`, `write` and `delete` file operations

- [x] Graphical User Interface (GUI)
  
  - [x] Implemented VESA BIOS Extension (VBE) & Video Graphic Array (VGA) hardware drivers.
  
  - [x] Able to load and display images stored in the hard disk as a file.

  - [x] Able to draw icons, buttons on the screen to support mouse click.
  
  - [x] Able to display graphical text on the screen.
    
  - [x] Suuported graphical shell.
  
  - [x] Display status bar at the bottom of the screen and create application windows (for example, multiple overlapping terminal windows which can be dragged by mouse).

- [x] Buddy Allocation System
  
  - [x] Implemented buddy allocation algorithm similar to the real Linux operating system.
  
  - [x] Able to allocate reasonable amount of free memory space to the user programs when there's a request (system call) from user programs.

