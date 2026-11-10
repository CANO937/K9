# The Core9 Kernel
The Core9 Kernel provides the foundational core of the K9 operating system. Implementing a hybrid kernel architecture, it synthesizes the modular isolation and security paradigms of a microkernel with the high-throughput performance characteristics of a monolithic kernel. The internal design is strictly object-oriented, encapsulating system resources, active processes, and hardware peripherals into discrete logical entities. This architectural framework delivers a robust, highly scalable, and optimized substrate engineered for modern computing architectures.
```
WindowsNT  ──────┐
UNIX       ──────┤
Plan9      ──────┤
BeOS       ──────┼──────> K9
OS/2       ──────┤
RSX-11M    ──────┤
BSD        ──────┘
```

# Supported Filesystems
- FAT32
- ExFAT
- USTAR (Initial Ramdisk)
- K9FS