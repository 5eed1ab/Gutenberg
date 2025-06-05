# [Gutenberg](https://en.wikipedia.org/wiki/Johannes_Gutenberg)
5E:ED:1A:B0:00:91
### [FreeBSD-14.2-RELEASE](https://docs.freebsd.org/en/books/handbook/bsdinstall/#bsdinstall-usb) usb drive
#### from MacOS
```zsh
curl -O https://download.freebsd.org/releases/amd64/amd64/ISO-IMAGES/14.2/FreeBSD-14.2-RELEASE-amd64-dvd1.iso
diskutil list
diskutil unmount /dev/disk5s1   
sudo dd if=FreeBSD-14.2-RELEASE-amd64-dvd1.iso of=/dev/disk5 bs=1M conv=sync
```
### [i3](https://i3wm.org/docs/)
#### [root](https://docs.freebsd.org/en/articles/new-users/#in-and-out)
```
pkg install sudo i3 i3status i3lock dmenu xorg drm-kmod

visudo # for learning %wheel ALL=(ALL:ALL) NOPASSWD: ALL

cat << EOF >> /etc/rc.conf
hald_enable="YES"
dbus_enable="YES"
kld_list="i915kms"
EOF

reboot
echo "exec /usr/local/bin/i3" >> .xinitrc
startx
```
### [punchcutting](https://github.com/punchcutting)
```
echo "exec /usr/local/bin/i3" >> .xinitrc
startx
```

### [Gitea](https://docs.gitea.com/installation/install-from-package#freebsd)
### [vscode](https://freebsdfoundation.org/resource/how-to-use-vs-code-on-freebsd/)
