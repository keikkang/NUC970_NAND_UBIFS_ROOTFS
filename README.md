# How to configure ubifs format rootfs in NUC970 Series

### 1. Configure linux-menuconfig 

#### 1. Deselect Initial RAM filesystem and RAM disk
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/441a6ea9-aa99-4912-9927-ac3cbc963b74)

#### 2. Default kernel command string 
Using this string : bootargs=noinitrd ubi.mtd=2 root=ubi0:user rw rootfstype=ubifs console=ttyS0,115200n8 rdinit=/sbin/init mem=64M mtdparts=nand0:0x200000@0x0(u-boot),0x1400000@0x200000(kernel),-(user)
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/f45fcae9-378d-48b6-9057-7568f2fdeecd)

#### 3. Select Memory Tchnology Deviced (MTD) support
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/70da42be-ec33-4508-aa8c-66f14c9c8878)

#### 4. Select Command line partition table parsing / Caching block device access to MTD devices / NAND Deivce SUPPORT / Enable UBI 
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/e8d44507-4f32-4815-8592-20c49aef1544)


#### 5. Select Nuvoton NUC970/N9H30 FMI function selection 
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/ff8237fe-ed28-4102-a3e4-bd3d61f94c08)

#### 6. Nuvoton NUC970/N9H30 MTD NAND (Port C)
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/f4eefc3c-5ad7-484b-b9bc-e5e7353c6c32)

#### 7. Miscellaneous filesystems → UBIFS file system support
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/4a4d5cda-92cd-409e-8efc-fd39c8b56adc)

### 2. Make ubifs img
