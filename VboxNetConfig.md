  sudo nano /etc/netplan/00-installer-config.yaml
  

```
  network:
    ethernets:
      eth1:
        dhcp4: no
        addresses:
          - 192.168.1.101/24  
        nameservers:
          addresses:
            - 8.8.8.8           
            - 8.8.4.4
      enp1s0:
        dhcp4: no
        addresses:
          - 10.0.2.14/24        
        gateway4: 10.0.2.1      
        nameservers:
          addresses:
            - 8.8.8.8
            - 8.8.4.4
    version: 2
```

  sudo netplan apply
  
  sudo ip link set eth1 up
  
  sudo ip link set enp1s0 up
