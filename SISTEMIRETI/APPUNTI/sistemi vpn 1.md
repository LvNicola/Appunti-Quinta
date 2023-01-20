

## 1 
Router(config)#router rip
Router(config-router)#no auto-summary
Router(config-router)#network 192.168.2.0
Router(config-router)#network 10.1.1.0
Router(config-router)#version 2
Router(config-router)#exit
Router(config)#exit
Router#
%SYS-5-CONFIG_I: Configured from console by console

Router#show crypto isakmp policy

 
Global IKE policy
Default protection suite

encryption algorithm: DES - Data Encryption Standard (56 bit keys).

hash algorithm: Secure Hash Standard

authentication method: Rivest-Shamir-Adleman Signature

Diffie-Hellman group: #1 (768 bit)

lifetime: 86400 seconds, no volume limit

## 2
Router#conf t
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#access-list 120 permit ip 192.168.2.0 0.0.0.255 192.168.3.0 0.0.0.255
Router(config)#crypto isakmp policy 1
Router(config-isakmp)#encryption aes 256
Router(config-isakmp)#authentication pre-share
Router(config-isakmp)#group 5
Router(config-isakmp)#exit

Router(config)#crypto isakmp key vpnpw1 address 10.2.2.2
Router(config)#crypto ipsec transform-set VPN-SET esp-aes esp-sha-hmac
Router(config)#crypto map VPN-MAP 10 ipsec-isakmp
Router(config-crypto-map)#description VPN connection to Router4
Router(config-crypto-map)#set peer 10.2.2.2
Router(config-crypto-map)#set transform-set VPN-SET
Router(config-crypto-map)#match address 120
Router(config-crypto-map)#exit

## 3
Router(config)#
Router(config)#interface Serial0/1/1
Router(config-if)#crypto map VPN-MAP

*Jan 3 07:16:26.785: %CRYPTO-6-ISAKMP_ON_OFF: ISAKMP is ON

Router(config-if)#end
Router#

%SYS-5-CONFIG_I: Configured from console by console
