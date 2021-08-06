# hdemo
Demo role for ansible hardening basics

1. Create a NAT network on Your windows box using powershell:
   <pre>
   New-VMSwitch -SwitchName "xmpnet" -SwitchType Internal
   New-NetIPAddress -IPAddress 192.168.66.1 -PrefixLength 24 -InterfaceAlias "vEthernet (xmpnet)"
   New-NetNat -Name xmpNAT -InternalIPInterfaceAddressPrefix 192.168.66.0/24
   </pre>
   It is expected that your VMs are connecting to the 192.168.66.0/24 network and sporting Fedora linux
2. This role is intended to run against the hosts (virtual machines) of that network
