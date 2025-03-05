# pihole_v5_patch
patch pihole v5 installer. otherwise, pihole will install the latest pihole v6

# instructions
please use at your own risk.

```
rm -rf /var/www/html/admin
rm -rf /etc/.pihole
wget https://github.com/pi-hole/pi-hole/archive/refs/tags/v5.18.4.zip
unzip -x v5.18.4.zip
wget https://raw.githubusercontent.com/baldwinsung/pihole_v5_patch/refs/heads/main/installer.patch
patch pi-hole-5.18.4/automated\ install/basic-install.sh < installer.patch
cd pi-hole-5.18.4/automated\ install/
./basic-install.sh
```

# credits

thank you to davide-italty for posting at https://discourse.pi-hole.net/t/how-to-install-any-v5/77255/4 
