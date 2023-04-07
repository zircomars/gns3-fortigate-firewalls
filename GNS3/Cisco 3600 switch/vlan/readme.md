# VLAN

Perus luodaan vlan id , sekä tässä on ladattu/lisätty <b>Cisco 3600 Etherswitch</b>


## Pien komento cheat sheet

ESW1#show vlan-switch

ESW1# conf t
ESW1(config)#

ESW1(config)#int vlan 10 <br>
ESW1(config-if)#name vlan10


ESW1#sh int status br>
Port    Name               Status       Vlan       Duplex Speed Type <br>
Fa1/0                      connected    1            full     100 10/100BaseTX <br>
Fa1/1                      connected    1            full     100 10/100BaseTX <br>
