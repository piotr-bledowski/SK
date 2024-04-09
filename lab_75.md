# A

## Router 1

enable

conf t

int fa0/0

ip address 200.200.200.1 255.255.255.0

no sh

int fa0/1

ip address 200.200.201.1 255.255.255.0

no sh

int loopback 3

ip address 100.100.101.1 255.255.255.0

no sh

int loopback 4

ip address 100.100.102.1 255.255.255.0

no sh

exit

ip routing

ip classless

router eigrp 1234

network 200.200.200.0 255.255.255.0

network 200.200.201.0 255.255.255.0

network 100.100.101.0 255.255.255.0

network 100.100.102.0 255.255.255.0

exit

exit


## Router 2

enable

conf t

int fa0/0

ip address 200.200.200.2 255.255.255.0

no sh

int fa0/1

ip address 200.200.201.2 255.255.255.0

no sh

int loopback 1

ip address 100.100.103.1 255.255.255.0

no sh

int loopback 2

ip address 100.100.104.1 255.255.255.0

no sh

exit

ip routing

ip classless

router eigrp 1234

network 200.200.200.0 255.255.255.0

network 200.200.201.0 255.255.255.0

network 100.100.103.0 255.255.255.0

network 100.100.104.0 255.255.255.0

exit

exit


