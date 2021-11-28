# omg LAN BUT V??
---
yeah, LAN but virtual

So imagine you have a big companies with different departments. Everyone is connected to the same network, everybody can access everybody else's stuff. While small companies might find this convenient, big departments are having [[Law of supply|diminishing returns]], and it is now more of a nuisance than a convenience. 

Your slaves are waging war against each other, people come to work everyday, spend 5 hours tryna find their files, and everything starts to fall apart.

Yeah, VLAN saves the day.

### HOW VLAN DO DAT??
First step to solving this problem is to set up individual LANs for each department, and connect the switch of every LAN to a central switch, to allow communication when required.

Second step is to yeet the cables, and bring in the VLAN, which can be used to partition the LANs, where every department is separated into logical separate networks (Which i will call LSNs). Each LSN cant see computer systems of other LSNs or their shared resources, without setups that allow them to.

### Comparing LAN and VLAN generally
![[LANvsVLAN.png]]

### Comparing LAN and VLAN that uses LSNs
![[LANvsVLANLSN.png]]