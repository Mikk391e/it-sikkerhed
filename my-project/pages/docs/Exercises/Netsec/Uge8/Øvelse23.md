# Øvelse 23 - opnsense udforskning

## Information

Denne øvelse skal laves som gruppe. Formålet med øvelsen er i får et overblik over hvad opnsense er og hvad det kan udover at være en router.
Husk at dokumentere jeres svar på gitlab på en måde så andre kan bruge det. (screenshots og links er ok, husk at lave lidt tekst som supplement til screenshots)

## Instruktioner

Gennemgå dokumentationen for opnsense på https://docs.opnsense.org/ samtidig med at i finder tingene på jeres opnsense installation i proxmox.
Besvar følgende:

1. Hvilke features tilbyder opnsense?

    - Traffic Shaper
    - Captive portal
    - Forward Caching Proxy
    - Virtual Private Network
    - High Availability & Hardware Failover
    - Intrusion Detection and Inline Prevention
    - Built-in reporting and monitoring tools
    - Support for plugins
    - DNS Server & DNS Forwarder
    - DHCP Server and Relay
    - Dynamic DNS
    - Backup & Restore
    - Stateful inspection firewall
    - Granular control over state table
    - 802.1Q VLAn support
    - and more

2. Hvordan kan du kontrollere om din opnsense version har kendte sårbarheder?

    Opnsense har en integreret sårbarhedsscanner.

    ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2023/OpnsenseSec.png)


3. Hvad er lobby og hvad kan man gøre derfra?

    ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2023/OpnsenseLobby.png)

4. Kan man se netflow data direkte i opnsense og i så fald hvor kan man se det?

    Ja det kan man godt. Man kan bruge den indbyggede Netflow Analyzer ved navnet Insight
    ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2023/Insight.png)
    

5. Hvad kan man se omkring trafik i Reporting?

    Den nuværende mængde traffik, som kommer igennem ens firewall, målt i bits i sekundet (bps)
    Man kan også se, hvilket interface trafikken kommer igennem.

6. Hvor oprettes vlan's og hvilken IEEE standard anvendes?

    ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2023/VLANSetup.png)
    ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2023/IEEEStandards.png)


7. Er der konfigureret nogle firewall regler for jeres interfaces (LAN og WAN)? Hvis ja, hvilke?

    Der er konfigureret default firewall regler for begge interfaces.

    - LAN:
        sshlockout, hvor man ikke kan forbinde via ssh efter 6 forkerte forsøg i træk
    
        Allow access to DHCP Server

        Block all targeting port 0

    - WAN:
         Block all targeting port 0

         sshlockout, hvor man ikke kan forbinde via ssh efter 6 forkerte forsøg i træk

        Block bogon IPV4 networks from WAN (blokerer pakker fra falske ip addresser)

8. Hvilke slags VPN understøtter opnsense?

    IPsec
    OpenVPN
    WireGuard

9. Hvilket IDS indeholder opnsense?

    Suricata

10. Hvor kan man installere os-theme-cicada i opnsense?

    Inde i System/Firmware/Plugins. Her søger du bare efter os-theme-cicada

11. Hvordan opdaterer man firmware på opnsense?

    Inde i System/Firmware/Status check for updates

12. Hvad er nyeste version af opnsense?

    25.1.1

13. Hvilken ip version tildeles som default til hhv. LAN og WAN interface ved installation?

    IPV4

14. Hvilket OS er opnsense baseret på?

    FreeBSD, som er fork af M0n0wall

15. Hvad betyder live mode i opnsense?

    Det betyder, at Opnsense booter fra et media device i stedet for fra harddisken

16. Hvilket interface og ip adresse kan opnsense webinterfacet tilgås fra?

    LAN interfacet 192.168.1.1, men kan mærkeligt nok også tilgåes via WAN interfacet med addressen 10.56.18.233.

17. Er jeres opnsense nyeste version? Hvis ikke så opdater den til nyeste version :-)

    Nej, vores version er 25.1, imens den nyeste version er 25.1.1

## Ressourcer

Home network guy artikel [Beginner's Guide to Set Up a Home Network Using OPNsense](https://homenetworkguy.com/how-to/beginners-guide-to-set-up-home-network-using-opnsense/)

Home network guy artikel [12 Ways to Secure Access to OPNsense and Your Home Network](https://homenetworkguy.com/how-to/ways-to-secure-access-to-opnsense-and-your-home-network/)

Home network guy artikel [video playliste Set up a Full Network using OPNsense](https://youtube.com/playlist?list=PLZeTcCOrKlnDlyZCIxhFZukAnA0NNWL_I&si=HJTg7AshyBXFHQbB)