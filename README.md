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

- [x] Writable fs
  
  - [x] Disk read
    
    [ATA PIO Mode - OSDev Wiki](https://wiki.osdev.org/ATA_PIO_Mode)
  
          <mark>seems good</mark>
  
  - [x] Disk Write
    
    [ATA PIO Mode - OSDev Wiki](https://wiki.osdev.org/ATA_PIO_Mode)
    
    Plan to test after finishing EXT2 parser 
  
  - [x] EXT2 parser
    
     [The Second Extended File System (nongnu.org)](https://www.nongnu.org/ext2-doc/ext2.html)
    
    - [x] EXT2 read_file
    
    - [x] EXT2 create_file
    
    - [x] EXT2 modify_file
    
    - [x] EXT2 delete_file

- [x] GUI
  
  - [x] VBE & VGA hardware
    
    [Bochs VBE Extensions - OSDev Wiki](https://wiki.osdev.org/Bochs_Graphics_Adaptor)
    
    `info pci` on test machine
    
    add `-vga std` in QEMU CMDLINE
  
  - [x] Display images
    
    [Loading Icons - OSDev Wiki](https://wiki.osdev.org/Loading_Icons)
  
  - [x] Draw icons, buttons
    
    [Loading Icons - OSDev Wiki](https://wiki.osdev.org/Loading_Icons)
  
  - [x] Draw text
    
    [VGA Fonts - OSDev Wiki](https://wiki.osdev.org/VGA_Fonts)
  
  - [x] Draw status bar, Windows
  
  - [x] Graphical Shell
  
  - [x] With mouse integrated
    
    [Mouse Input - OSDev Wiki](https://wiki.osdev.org/Mouse_Input)

- [x] Buddy allocation
  
    [Buddy memory allocation - Wikipedia](https://en.wikipedia.org/wiki/Buddy_memory_allocation)
  
  - [x] Algorithmic correct
  
  - [x] Actually allocated to user programs

- [x] Sound drive
  
  [Sound Blaster 16 - OSDev Wiki](https://wiki.osdev.org/Sound_Blaster_16) (REMEMBER TO APPEND HARDWARE CONFIG INTO QEMU CMDLINE)
