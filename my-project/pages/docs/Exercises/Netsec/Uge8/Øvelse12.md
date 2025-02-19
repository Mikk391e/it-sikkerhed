# Øvelse 12 - Protokoller og OSI modellen

## Information

Dette er en gruppeøvelse.

I denne øvelse skal i som gruppe bruge wireshark til at finde eksempler på protokoller i den trafik i sniffer med wireshark.
Der findes mange protokoller der anvendes til at kommunikere over netværk men protokoller bliver også misbrugt af trusselsaktører til forskellige typer af angreb.
Som eksempel kan TCP misbruges i forbindelse med Denial-Of-Service angreb hvor en eller flere enheder sender SYN forespørgsler til en modtager og på den måde overbelaster modtageren.
Du kan læse mere her: https://www.cloudflare.com/learning/ddos/syn-flood-ddos-attack/ Formålet med øvelsen er at få en forståelse for netværksprotokoller og dermed senere kunne teste netværk for angreb rettet mod protokoller. Øvelsen giver jer også kendskab og rutine i at anvende wireshark og dermed få en forståelse for hvad det betyder at sniffe netværks trafik.

I skal bruge jeres kali maskine forbundet til opnsense routeren som i satte op i [OPNsense på virtual box](https://ucl-pba-its.gitlab.io/25f-its-nwsec/exercises/20_opsense_vbox/) øvelsen

## Instruktioner

1. I kali åbn wireshark og lyt på eth0 interfacet indtil i har sniffet en god mængde trafik. Hvis der ikke kommer meget trafik kan i åbne browseren på kali og browse et par sider (gerne nogen der bruger http og ftp hvis i kan finde det) så burde der komme en del trafik.

2. Tryk på stop knappen i wireshark (den røde firkant)

3. Gem trafikken som en .pcapng fil på kali maskinen i documents mappen

    ![Image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2012/Screenshot%202025-02-19%20110706.png)

4. Lav en liste over de protokoller der optræder i trafikken og placer protokollerne i OSI modellen. (her kan statistics menuen hjælpe med at danne et overblik over protokoller)
![wireshark protocols](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2012/wireshark_protocol_hierachy.png)

 - HTTP
 - DNS
 - OCSP
 - QUIC
 - TCP
 - TLSv1.2
 - TLSv1.3

5. Find minimum et eksempel, med kildehenvisning, på hvordan en af jeres fundne protokoller kan misbruges af en trusselsaktør, husk at være kritiske med den kilde i anvender til at underbygge jeres påstand.

Vi har valgt at kigge på QUIC protokollen.

>QUIC uses UDP for ports and connectionless transport, then adds the resiliency of TCP, the security of TLS 1.3, sprinkles in a dash of commands and version control from protocols like SMB, and then mixes in a set of new protocol concepts and efficiencies to create something entirely unique in the protocol world.
>
> -- [James Kehr, medarbjer hos Microsoft](https://techcommunity.microsoft.com/blog/networkingblog/whats-quic/2683367)

For at se om QUIC er sårbart, har vi lavet noget litteratursøgning, og fandt til følgende studie:
[Revisiting QUIC attacks: a comprehensive review on QUIC security and a hands-on study (Chatzoglou Et al. 2023)](https://link.springer.com/article/10.1007/s10207-022-00630-6)

[Link til Github](https://github.com/efchatz/QUIC-attacks/blob/main/quic-flooding/quic-flooding.sh)

Studiet er en metaanalyse af andre studier på området. 3 af forskerne bag studiet er associeret med et universitet i Grækenland, mens den sidste forsker arbejder i EU kommissionen.

Ifølge studiet, findes der mange forskellige svagheder ved protokollen, et af disse værende et form for DOS angreb: 
>The third attack tested by the authors was a crypto stream offset assault, where they injected a four character string, that is, “REJ\0” into the handshake message. This addition was enough to make the handshake fail and prevent the establishment of a QUIC connection between the client and the server either by denying access to the requested application or forcing the client to fall back to a TCP/TLS connection. Additionally, this attack was correlated to a TCP ACK flooding attack, in which an attacker sends multiple acknowledged (ACK) responses to the server to confuse it and drop the connection (Chatzoglou Et al. 2023).


6. Vi laver kort opsamling på klassen baseret på spørgsmål fra jer.
Jeg kigger på jeres gitlab dokumentation og giver feedback næste undervisningsgang.

## Ressourcer

Hvis i har brug for at genopfriske wireshark kan i bruge:

[THM: Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics)

[Wireshark docs](https://www.wireshark.org/docs/)