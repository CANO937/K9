# Bootsequence
```
─── Limine
    ├── Ramdisk                      ──── Dropped after Manager Init
    └── Core9
        ├── SyS/Init                 ──── Dropped after Manager init
        ├── Boot Dirvers             ──── Dropped after Manager Init
        │   ├── SyS/FAT32            ──┐
        │   ├── SyS/ExFAT            ──┼─ Filesystems
        │   ├── SyS/K9FS             ──┘
        │   ├── SyS/SATA             ──┐
        │   ├── SyS/NVMe             ──┼─ Disks
        │   ├── SyS/IDE              ──┘
        │   ├── SyS/USB              ──┐
        │   ├── SyS/UART             ──┼─ Ports
        │   └── SyS/VGA              ──┘
        ├── SyS/Manager
        │   ├── OVR/ResourceManager  ──── ACRM Management (Ram, Cores, Threads)
        │   └── OVR/Orchestrator     ──── TCVPR Management (Task Contained Virtual Protection Rings)
        └── Runtime Drivers
            ├── SyS/FAT32            ──┐
            ├── SyS/ExFAT            ──┼─ Filesystems
            ├── SyS/K9FS             ──┘
            ├── SyS/SATA             ──┐
            ├── SyS/NVMe             ──┼─ Disks
            ├── SyS/IDE              ──┘
            ├── SyS/USB              ──┐
            ├── SyS/UART             ──┼─ Ports
            └── SyS/VGA              ──┘
```
```
ACRM (Absolute Communist Resource Management): Communism! Local Execution Queues for CPUs (per-Core Runqueues) BUT the ResourceManager controls the queues. If there is a completely empty queue in CPU7, for instance, and a clogged one in CPU4, it performs a thread switch and moves some processes to CPU7 to balance the load, without importing one of the most difficult algorithms out there: Work Stealing.
```
```
LK (Lazy Kernel): Design philosophy centered on minimizing kernel intervention, ensuring it manages only the absolute bare essentials of the system.
```
        