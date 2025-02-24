# Øvelse 18 - Udforskning af opnsense cli og webinterface

## Information

I denne øvelse skal du oprette forbindelse til opnsense cli og webinterface.
Jeg kalder opnsense for en router, men i virkeligheden er det meget mere end det, feks. en firewall, DNS proxy, IDS/IPS og meget mere.

Du kan danne dig et overblik på https://opnsense.org/

## CLI interface

Opnsense Commmand Line Interface (cli) bruges til at administrere opnsense på den maskine opnsense er installeret på. I daglig tale kaldes det også konsoladgang eller konsolinterface.

CLI vil typisk være det interface du bruger til at konfigurere routeren første gang. Her vil du konfigurere netværksadresser, netværksstørrelser, DHCP mm. for de enkelte netværksinterfaces (NIC).

Jeg har allerede konfigureret opnsense maskinen for jer. Den har 4 NIC's som hedder hhv. LAN, OPT1, OPT2 og WAN. Navngivningen er tildelt af opnsense og jeg har valgt at beholde navnene.

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2018/Screenshot%202025-02-24%20110825.png)
*opnsense cli interface*

WAN er konfigureret til at modtage en IP adresse fra DHCP, det vil i dette tilfælde betyde at virtualbox tildeler en "WAN" adresse som oversættes af virtualbox ved hjælp af NAT.

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2018/Screenshot%202025-02-24%20111243.png)
*opnsense virtualbox network settings adapter1 (WAN)*

LAN, OPT1 og OPT 2 er alle forbundet til interne netværk i virtualbox. På den måde vil det være opnsense der fungerer som router for de 3 interfaces/netværk.
Jeg har valgt at kalde dem intnet 1 - 3 i virtualbox. Det er ikke så vigtigt hvilket navn de har, så længe de kan identificeres.

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2018/Screenshot%202025-02-24%20111428.png)
*opnsense virtualbox network settings adapter 2, 3, 4 (LAN, OPT1, OPT2)*

## Web interface

pr. default er opnsense web interfacet kun tilgængeligt fra interne netværk, altså ikke fra WAN siden. Det vil sige at du skal bruge en maskine som er tilsluttet et internet netværk, altså alle undtaget WAN.

Inden du kan tilgå web interfacet skal du logg ind i opnsense. Her har jeg valgt at beholde default credentials fordi routeren bruges i et virtuelt miljø som kun jeg har adgang til.

Det er faktisk dårlig praksis at gøre det selvom det er et test miljø. Det ses alt for mange gange at default brugernavn:password ikke ændres når test miljøet migreres til produktion.
Det er en længere debat som også bør inkludere vigtigheden af at implementere Multi Factor Authentication (MFA) som opnsense selvfølgelig også understøtter.

Du kan logge ind i opnsense via web med disse credentials: **root:opnsense**

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2018/Screenshot%202025-02-24%20111604.png)

*opnsense web login*

Web interfacet kan være lidt overvældende hvis du ikke har brugt opnsense før. Det er fra web interfacet at det meste af opnsense funktionaliteten konfigureres.

Det er også fra webinterfacet du kan se logs og statistik over netværkstrafik, firewall og systemhændelser.

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2018/Screenshot%202025-02-24%20111701.png)
*opnsense web dashboard*

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2018/Screenshot%202025-02-24%20111754.png)

## Instruktioner

1. Log på CLI og kontroller at interfaces og netværks adresser stemmer overens med netværksdiagrammet.
    * Noter WAN adressen
    * Hvis noget ikke stemmer overens så fejlsøg (husk at spørge om hjælp)
    * Hvis der er noget du ikke forstår, så spørg om hjælp!
    * Når du forstår diagram og CLI interface informationen så fortsæt til næste trin.
2. Log på web interfacet og gennemgå dokumentationen for opnsense på https://docs.opnsense.org/ samtidig med at i finder tingene på jeres opnsense installation i virtualbox.

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

## Link

* [opnsense dokumentation](https://docs.opnsense.org/)