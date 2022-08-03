# Tuya-OEM-PTZ-IPCamera
Adventures into the land of Tuya and rooting an OEM PTZ camera

# Root achieved, write up in the making.
## Send me a message on Discord if you can't wait that long ;)
```shell
  204 root      1428 S    telnetd
  292 root      1432 R    ps
[root@Zeratul:~]#

[root@Zeratul:~]# uname -a
Linux Zeratul 3.10.14-Archon #51 PREEMPT Fri Dec 24 09:50:57 CST 2021 mips GNU/Linux

[root@Zeratul:~]# cat /proc/cpuinfo
system type             : Indus_T31_QFN
machine                 : Unknown
processor               : 0
cpu model               : Ingenic Xburst V0.0  FPU V0.0
BogoMIPS                : 1391.00
wait instruction        : yes
microsecond timers      : no
tlb_entries             : 32
extra interrupt vector  : yes
hardware watchpoint     : yes, count: 1, address/irw mask: [0x0fff]
isa                     : mips32r1
ASEs implemented        :
shadow register sets    : 1
kscratch registers      : 7
core                    : 0
VCED exceptions         : not available
VCEI exceptions         : not available

Hardware                : isvp
Serial                  : 00000000 00000000 00000000 00000000

[root@Zeratul:~]# cat /proc/mtd
dev:    size   erasesize  name
mtd0: 00040000 00001000 "boot"
mtd1: 00058000 00001000 "tag"
mtd2: 00280000 00008000 "kernel"
mtd3: 00280000 00008000 "rootfs"
mtd4: 001c0000 00008000 "system"
mtd5: 00048000 00008000 "config"
mtd6: 00010000 00001000 "ae"
mtd7: 00040000 00001000 "audio"
mtd8: 00010000 00001000 "vd"
mtd9: 00800000 00008000 "all"

[root@Zeratul:~]# cat /proc/cmdline
console=ttyS2,115200n8 mem=42M@0x0 rmem=22M@0x2A00000 root=/dev/ram0 rw rdinit=/linuxrc mtdparts=jz_sfc:256K(boot),352K(tag),2560K(kernel),2560K(rootfs),1792K(system),288K(config),64K(ae),256K(audio),64K(vd),8M@0(all) lpj=6955008 quiet senv;[HW];ae_auto_learn=1;init_vw=1920;init_vh=1080;nrvbs=1;mode=0;is_h264=1;adc_value=100;select_mode=1;[UBIA];main_bitrate=1536;sub_bitrate=512;vide_flip=3;ai_vol=60;ao_vol=70;md_level=4;battery_cam=1;debug;ModelNum=237;sample=8000;[IR];ir_mode=auto;eenv; lzo_size=2597064 rd_start=0x80600000 rd_size=0x58ae00  ubootV=V017
```
