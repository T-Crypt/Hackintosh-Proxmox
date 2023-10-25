# HOW TO FIX HIGH CPU USAGE ON YOUR HACKINTOSH USING PROXMOX

This is for you to fix the High CPU Usage issue on your new way hackintosh using our new way with proxmox. 


```bash
sudo nano /etc/pve/qemu-server/[VMID].conf
```

For Intel CPUs
Add this to the end of your Hackintosh VM Args:

```bash
core, NATIVE
cores, NATIVE
cores, -smp 3,cores=1,sockets=3,threads=1,maxcpus=3
cores, NATIVE
cores, -smp 5,cores=1,sockets=5,threads=1,maxcpus=5
cores, -smp 6,cores=2,sockets=3,threads=1,maxcpus=6
cores, -smp 7,cores=1,sockets=7,threads=1,maxcpus=7
cores, -smp 8,cores=4,sockets=2,threads=1,maxcpus=8
cores, NATIVE
cores, -smp 9,cores=1,sockets=9,threads=1,maxcpus=9
cores, -smp 10,cores=2,sockets=5,threads=1,maxcpus=10
cores, -smp 11,cores=1,sockets=11,threads=1,maxcpus=11
cores, -smp 12,cores=2,sockets=3,threads=2,maxcpus=12
cores, -smp 13,cores=1,sockets=13,threads=1,maxcpus=13
cores, -smp 14,cores=2,sockets=7,threads=1,maxcpus=14
cores, -smp 15,cores=1,sockets=15,threads=1,maxcpus=15
cores, NATIVE
cores, -smp 17,cores=1,sockets=17,threads=1,maxcpus=17
cores, -smp 18,cores=2,sockets=9,threads=1,maxcpus=18
cores, -smp 19,cores=1,sockets=19,threads=1,maxcpus=19
cores, -smp 20,cores=2,sockets=5,threads=2,maxcpus=20
cores, -smp 21,cores=1,sockets=21,threads=1,maxcpus=21
cores, -smp 22,cores=2,sockets=11,threads=1,maxcpus=22
cores, -smp 23,cores=1,sockets=23,threads=1,maxcpus=23
cores, -smp 24,cores=2,sockets=6,threads=2,maxcpus=24
cores, -smp 25,cores=1,sockets=25,threads=1,maxcpus=25
cores, -smp 26,cores=2,sockets=13,threads=1,maxcpus=26
cores, -smp 27,cores=1,sockets=27,threads=1,maxcpus=27
cores, -smp 28,cores=2,sockets=7,threads=2,maxcpus=28
cores, -smp 29,cores=1,sockets=29,threads=1,maxcpus=29
cores, -smp 30,cores=2,sockets=15,threads=1,maxcpus=30
cores, -smp 31,cores=1,sockets=31,threads=1,maxcpus=31
cores, NATIVE
...
48 cores, -smp 48,cores=2,sockets=24,threads=1,maxcpus=48
48 cores, -smp 48,cores=2,sockets=12,threads=2,maxcpus=48
...
```
For AMD CPUs:

```
args: -device isa-applesmc,osk="ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc" -smbios type=2 -device usb-kbd,bus=ehci.0,port=2 -global nec-usb-xhci.msi=off -cpu host
```
