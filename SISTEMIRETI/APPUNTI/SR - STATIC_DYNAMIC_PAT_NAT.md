﻿## NAT Statico
Router>enable

Router #conf t

Router(config) #int g0/0

Router(config-if) #ip nat inside

Router(config-if) #exit

Router(config) #int g0/1

Router(config-if) #ip nat outside

Router(config-if) #exit

Router(config) #ip nat inside source static 10.1.1.1 170.168.2.2

Router(config) #ip nat inside source static 10.1.1.2 170.168.2.3

Router(config) #ip nat inside source static 10.1.1.3 170.168.2.4

Router(config) #ip nat inside source static 10.1.1.200 170.168.2.5

## NAT Dinamico

- Creiamo il pool di IP pubblici
- Creiamo ACI per gestire gli host della rete interna
- Associo ACI pool

Router>enable

Router #conf t

Router(config) #int g0/0

Router(config-if) #ip nat inside

Router(config-if) #exit

Router(config) #int g0/1

Router(config-if) #ip nat outside

Router(config-if) #exit

Router(config) #ip nat pool pubblico 170.168.2.2 170.168.2.254 netmask 255.255.255.0

Router(config) #access-list 1 permit 10.1.1.0 0.0.0.255

Router(config) #ip nat inside source list 1 pool pubblico

## PAT NAT

Router>enable

Router #conf t

Router(config) #int g0/0

Router(config-if) #ip nat inside

Router(config-if) #exit

Router(config) #int g0/1

Router(config-if) #ip nat outside

Router(config-if) #exit

Router(config) #access-list 1 permit 10.1.1.0 0.0.0.255

Router(config) #ip nat pool pubblico 170.168.2.2 170.168.2.254 netmask 255.255.255.0

Router(config) #ip nat inside source list 1 pool pubblico overload

> Se hai un solo IP pubblico, esegui quest'ultimo comando:
Router(config) #ip nat pool pubblico 170.168.2.2 170.168.2.2 netmask 255.255.255.0
