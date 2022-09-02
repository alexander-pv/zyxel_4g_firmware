
Unofficial Zyxel 4G firmware forked from `Dr.Acid`, source: http://forum.zyxmon.org

0. Load Dr. Acid firmware via Zyxel web
1. Format USB drive to ext2
2. Unpack `ext_init_4g_v1.gz` to the USB drive
3. Connect USB drive to Zyxel 4G, wait for journal message `opkg/linux installation finished`
4. Connect to device (init password `zyxel`):
```bash
$ ssh -o KexAlgorithms=diffie-hellman-group1-sha1 root@192.168.1.1
```


