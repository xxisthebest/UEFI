# MAC
�����Linuxϵͳ�н��а�װ����Mac����Ҫ��װһ�������
## VMware Fusion
## Ubuntu
### ����Զ�����ӿ��ƣ�ssh
��ϵͳ������
```
ifconfig
```
![alt text](image.png)
�õ�`ens160->inet`�Ķ˿ںţ���mac�д��նˣ�����
```
ssh wby@172.16.174.128
```
����ΪUbuntu���û����룬��������
```
(base) nancywang@xxs-book ~ % ssh wby@172.16.174.128
wby@172.16.174.128's password:
Welcome to Ubuntu 24.10 (GNU/Linux 6.11.0-8-generic aarch64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Mon Oct 21 02:33:28 PM UTC 2024

  System load:  0.0               Temperature:             11758.9 C
  Usage of /:   24.8% of 9.75GB   Processes:               245
  Memory usage: 7%                Users logged in:         0
  Swap usage:   0%                IPv4 address for ens160: 172.16.174.128


1 update can be applied immediately.
To see these additional updates run: apt list --upgradable
```
## ��¡�ֿ�
```
git clone https://github.com/tianocore/edk2.git
cd edk2
git submodule update --init
sudo apt install bison
sudo apt install iasl
sudo apt install uuid-dev
sudo apt install python3
sudo ln -s /usr/bin/python3 /usr/bin/python
sudo apt install alien
sudo wget https://www.nasm.us/pub/nasm/releasebuilds/2.16.03/linux/nasm-2.16.03-0.fc39.x86_64.rpm # �ڵ�ǰĿ¼������nasm

source edksetup.sh
make -C BaseTools //ֻ��Ҫִ��һ�μ��ɣ��״α���
build -a AARCH64 -t GCC5 -p ArmVirtPkg/ArmVirtQemu.dsc -b DEBUG
sudo apt install xorg # ��ubuntu�ϰ�װ
```
�ɹ���ʾ��
```
Fd File Name:QEMU_EFI (/home/wby/edk2/Build/ArmVirtQemu-AARCH64/DEBUG_GCC5/FV/QEMU_EFI.fd)

Generate Region at Offset 0x0
   Region Size = 0x1000
   Region Name = DATA

Generate Region at Offset 0x1000
   Region Size = 0x1FF000
   Region Name = FV

Generating FVMAIN_COMPACT FV

Generating FVMAIN FV
#######
Fd File Name:QEMU_VARS (/home/wby/edk2/Build/ArmVirtQemu-AARCH64/DEBUG_GCC5/FV/QEMU_VARS.fd)

Generate Region at Offset 0x0
   Region Size = 0x40000
   Region Name = DATA

Generate Region at Offset 0x40000
   Region Size = 0x40000
   Region Name = DATA

Generate Region at Offset 0x80000
   Region Size = 0x40000
   Region Name = None

GUID cross reference file can be found at /home/wby/edk2/Build/ArmVirtQemu-AARCH64/DEBUG_GCC5/FV/Guid.xref

FV Space Information
FVMAIN [99%Full] 6545408 (0x63e000) total, 6545368 (0x63dfd8) used, 40 (0x28) free
FVMAIN_COMPACT [55%Full] 2093056 (0x1ff000) total, 1152352 (0x119560) used, 940704 (0xe5aa0) free

- Done -
```
��дsh�ļ��������û�����
```
export WORKSPACE=$PWD
export PACKAGES_PATH=/home/wby/edk2
export IASL_PREFIX=/home/wby/acpica/generate/unix/bin/
export PYTHON_COMMAND=/usr/bin/python3
export GCC5=/usr/bin/gcc
```

### ����
1��
```
/bin/sh: 1: /home/wby/edk2/acpica/generate/unix/bin/iasl: not found
make:
```
ԭ��iasl��·�����⣬��Ҫ��������IASL_PREFIX��·��Ϊ/home/wby/acpica/generate/unix/bin/

# Windwos --SUCCESS
����[[ UEFI���� ] Linux ���� ( Ubuntu ) ���� EDK2 ��������](https://blog.csdn.net/weixin_44139099/article/details/140681442)�Ĳ������У�������ɹ���ע�������һ���ط�����Ҫcd��

# ECC
<https://github.com/tianocore/tianocore.github.io/wiki/ECC-tool>
������߿��԰������������ʽ����
