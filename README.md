# How to configure ubifs format rootfs in NUC970 Series

### 1. Configure linux-menuconfig 

#### 1. Deselect Initial RAM filesystem and RAM disk
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/441a6ea9-aa99-4912-9927-ac3cbc963b74)

#### 2. Default kernel command string 
Using this string : bootargs=noinitrd ubi.mtd=2 root=ubi0:user rw rootfstype=ubifs console=ttyS0,115200n8 rdinit=/sbin/init mem=64M mtdparts=nand0:0x200000@0x0(u-boot),0x1400000@0x200000(kernel),-(user)
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/f45fcae9-378d-48b6-9057-7568f2fdeecd)

#### 3. Select Memory Tchnology Deviced (MTD) support
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/70da42be-ec33-4508-aa8c-66f14c9c8878)

#### 4. Select Command line partition table parsing / Common interfacae to block layer for MTD 'translation layers' / NAND Deivce SUPPORT / Enable UBI 

![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/b80c6b0c-fcf1-471b-80a1-539db2bba9ad)

#### 5. Select Nuvoton NUC970/N9H30 FMI function selection 
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/ff8237fe-ed28-4102-a3e4-bd3d61f94c08)


#### 6. Nuvoton NUC970/N9H30 MTD NAND (Port C)
![image](https://github.com/keikkang/NUC980_GINU_BSP/assets/108905975/83d0c313-7589-4b92-adff-ac305e78dd97)

