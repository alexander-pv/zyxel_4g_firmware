
Unofficial Zyxel 4G firmware forked from `Dr.Acid`, source: http://forum.zyxmon.org

0. Use additional laptop to share Internet via Ethernet to the Zyxel 4G
1. Load Dr.Acid firmware via Zyxel web
2. Format USB drive to ext2 (gparted)
3. Unpack `ext_init_4g_v1.gz` to the USB drive
4. Connect USB drive to Zyxel 4G, wait for journal message `opkg/linux installation finished`
5. Connect to device (init password `zyxel`):
```bash
$ ssh -o KexAlgorithms=diffie-hellman-group1-sha1 root@192.168.1.1
```
6. Update opkg: add to `/media/DISK_A1/system/etc/opkg.conf` new address: `http://zyxware.zyxmon.org/binary-packages-r2`
```bash
$ opkg update && opkg upgrade
$ opkg install openssl
```

