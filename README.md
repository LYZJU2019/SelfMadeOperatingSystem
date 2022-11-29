# Project Description

I developed the core of an operating system (OS), including the boot stage setup, paging machenisim, PIC interface between hardware devices and OS software, in-memory file system and disk file system implementation, system call interface between user programs and OS as well as scheduler and multiple terminal. (See the full feature list below)

## Basic features

✅ Global Descriptor Table (GDT), Local Descriptor Table (LDT), Task State Segment (TSS) initialized, use GRUB to boot the OS image file.
 
✅ Enable 4KB user pages (video memory and program stacks) and 4MB OS page.

✅ Programmable Interrupt Controller (PIC) initialized to enable keyboard, mouse, sound drive, Real-Time Clock (RTC), Periodic Interrupt Timer (PIT), etc. 
 
✅ Interrupt Descriptor Table (IDT) initialized and the items associated with those hardware devices are filled.
 
✅ Memory buffer operations (open, read, write, close) implemented after reading file data from the in-memory file system.
 
✅ Implemented System call linkage (in Assembly) to provide OS services to the user programs.
 
✅ Implemented Process Control Block (PCB) to support the execution of user programs.
 
✅ Implemented scheduler to support task switching.

✅ Supported multiple terminals with virtually separate keyboard buffer, video memory, cursor, etc. Such that one program can execute without noticing the execution of other programs.

## Advanced features
- More hardware devices supported

    ✅ PS2 mouse

    ✅ sound drive

- Writable File System
  
   ✅ Implemented hard disk driver to support reading chunks of data from the hard disk and writing chunks of data into the hard disk
  
   ✅ Implemented The Second Extended File System (EXT2) parser to support `read`, `open`, `close`, `write` and `delete` file operations

- Graphical User Interface (GUI)
  
  ✅ Implemented VESA BIOS Extension (VBE) & Video Graphic Array (VGA) hardware drivers.
  
  ✅ Able to load and display images stored in the hard disk as a file.

  ✅ Able to draw icons, buttons on the screen to support mouse click.
  
  ✅ Able to display graphical text on the screen.
    
  ✅ Suuported graphical shell.
  
  ✅ Display status bar at the bottom of the screen and create application windows (for example, multiple overlapping terminal windows which can be dragged by mouse).

- Buddy Allocation System
  
  ✅ Implemented buddy allocation algorithm similar to the real Linux operating system.
  
  ✅ Able to allocate reasonable amount of free memory space to the user programs when there's a request (system call) from user programs.

