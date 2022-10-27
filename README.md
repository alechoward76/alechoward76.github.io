# alechoward76.github.io

Step 1: Arch Linux Installation & Launch
  - Acquire an installation image and verify its signature
  - Open the download in VMware
  - In the launch settings, select Other Linux 5.x Kernel 64-bit as the OS
  - Allocate 2GB of RAM and 20GB of HDD space 
  - After creating the VM, edit the .vmx file and insert: firmware="efi" as the second line of the file
  - Now we are able to run the virtual machine

Step 2: Partitioning the Disk
  - List the disk using the command: fdisk -l
  - My disk was assigned to /dev/sda , so I used this command to begin partitioning: fdisk /dev/sda
  - I made three partitions: sda1 for the EFI system partition, sda2 for Linux swap, and sda3 for root
 
 Step 3: Formatting Partitions: 
  - In order to format the EFI system partition, I used this command: mkfs.fat -F 32 /dev/efi_system_partition
  - To format the swap partition, I used this command: mkswap /dev/swap_partition
  - Finally, to format the root partition, this command was used: mkfs.ext4 /dev/root_partition

Step 4: Mounting the File Systems
  - 

