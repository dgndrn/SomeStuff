ip addr add [ip_address] dev [interface]

sudo ifconfig [interface] up

sudo ip link set [interface] up

sudo nano /etc/netplan/config.yaml
---

network:

  version: 2

  renderer: networkd

  ethernets:

    eth1:

      addresses:

        - 192.168.56.66/24

      nameservers:

         addresses:

           - 8.8.8.8

      routes:

        - to: default

          via: 10.0.2.2



  sudo netplan try
  
  sudo netplan apply



  
ip link set enp0s8 up

/usr/sbin/dhclient enp0s8

nano /etc/network/interfaces

auto enp0s8

iface enp0s8 inet dhcp
  
edit ~/.bashrc
export PATH=$PATH:{path}
source ~./bashrc


