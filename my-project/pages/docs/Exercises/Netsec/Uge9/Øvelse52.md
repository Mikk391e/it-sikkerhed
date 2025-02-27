# Øvelse 52 - Praktisk netværkssegmentering i virtualbox med opnsense

## Information

Øvelsen er individuel.

I denne øvelse skal du arbejde praktisk med segmentering af netværk i opnsense.
Formålet er at lære hvordan du kan udvide opnsense med et ekstra netværksinterface og tilhørende netværk.
På den måde vil din opnsense router, efter udførelse af øvelsen, have to netværkssegmenter. LAN og management.

## Instruktioner

1. Sluk for opnsense VM. Tilføj et ekstra netværksinterface på samme måde som da du konfigurerede maskinen i OPNsense i virtualbox
2. Tilslut netværksinterfacet til intnet3.
3. Tænd for opnsense og konfigurer det nye interface som nedenstående:

Assign nyt interface, kald det `management`

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_1.png)

*Konfigurer interfacet som følgende*

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_3.png)

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_4.png)

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_5.png)

*Tænd for DHCP på netværket og tildel følgende DHCP range*

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_6.png)

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_7.png)
4. Tilslut en ny VM til vmnet3 og bekræft at maskinen får tildelt en IP i den ip range du har konfigureret på interfacet.

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_8.png)

![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/opnsense_new_network_9.png)


![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2052/Screenshot%202025-02-26%20152310.png)

## Ressourcer

- [OPNsense docs - Interfaces](https://docs.opnsense.org/interfaces.html)

- [How to Create a Basic DMZ (Demilitarized Zone) Network in OPNsense](https://homenetworkguy.com/how-to/create-basic-dmz-network-opnsense/)