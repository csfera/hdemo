# hdemo
Demo role for ansible hardening basics

1. Create a NAT network on Your windows box using powershell:
   New-VMSwitch -SwitchName "xmpnet" -SwitchType Internal
   New-NetIPAddress -IPAddress 192.168.66.1 -PrefixLength 24 -InterfaceAlias "vEthernet (xmpnet)"
   New-NetNat -Name xmpNAT -InternalIPInterfaceAddressPrefix 192.168.66.0/24
