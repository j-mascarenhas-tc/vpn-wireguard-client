# Instalação Wireguard Client Gui - Ubuntu



## Ubuntu 20.04

#### Install the needed packages to build and use the plugin:



```shell
sudo apt install wireguard git dh-autoreconf libglib2.0-dev intltool build-essential libgtk-3-dev libnma-dev libsecret-1-dev network-manager-dev resolvconf
```



#### Clone the plugin from github, compile and install it:

```shell
git clone https://github.com/max-moser/network-manager-wireguard
cd network-manager-wireguard
./autogen.sh --without-libnm-glib

./configure --without-libnm-glib --prefix=/usr --sysconfdir=/etc --libdir=/usr/lib/x86_64-linux-gnu --libexecdir=/usr/lib/NetworkManager --localstatedir=/var

make   
sudo make install
```



#### Now the Network VPN Menus have Wireguard as an option



![network manager](https://discussion.scottibyte.com/uploads/default/original/1X/2bd021cbe18877b6ad83235de8d2e1452460ad7f.png)