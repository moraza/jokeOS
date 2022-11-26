# jokeOS
An Open Source Operating System designed to deliver Dad Jokes

# Compiling from Source (on Linux)
- Install Docker
- Enter Build System by executing following commands:
```bash
docker build buildsys -t jokeos-buildsys
docker run --rm -it -v `pwd`:/root/env:z jokeos-buildsys
```
- Build ISO by running following command:
```bash
make build-x86_64
```
- This will result the creation of a bootable ISO in dist/x86_64 named jokeOS.iso
- This ISO can be booted on a physical device, Virtualization platform (VirtualBox, VMware Workstation, Hyper-V) and QEMU.
- To boot this on QEMU, run the following command:
```bash
qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso
```