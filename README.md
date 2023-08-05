# strongSwan-on-OpenWrt

# enable bypass-lan 

```
sed -i "\$a\src-git my_strongswan https://github.com/xxooxxooxx/strongSwan-on-OpenWrt.git" $(pwd)/feeds.conf.default

./scripts/feeds update my_strongswan
#./scripts/feeds install -a -p my_strongswan
./scripts/feeds uninstall strongswan
./scripts/feeds install -p my_strongswan strongswan

make package/strongswan/compile -j

ls bin/packages/x86_64/my_strongswan/
```
