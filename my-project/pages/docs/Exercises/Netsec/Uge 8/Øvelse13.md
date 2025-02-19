# Øvelse 13 - Protokolforståelse

## Information

Dette er en gruppeøvelse.

I denne øvelse får i et dybere kendskab til hvad en protokol er og hvordan den er opbygget.
Øvelsen tager udgangspunkt i Transmission Control Protocol (TCP) som er en [IETF standard](https://www.ietf.org/) beskrevet i RFC [(Request For Comments)](https://en.wikipedia.org/wiki/Request_for_Comments) 9293.
TCP er ikke krypteret og derfor vil data i TCP pakker kunne læses i "klartekst" hvis ikke det krypteres. Dette kan gøres ved for eksempel at anvende Transport Layer Security (TLS)

## Instruktioner

1. I kali åbn wireshark og lyt på eth0 interfacet indtil i har sniffet en god mængde trafik. Hvis der ikke kommer meget trafik kan i åbne browseren på kali og browse et par sider, så burde der komme en del trafik.

2. Tryk på stop knappen i wireshark (den røde firkant)

3. Gem trafikken som en `.pcapng` fil på kali maskinen i documents mappen

4. Find et TCP 3-way handshake i trafikken og sammenlign wireshark dataen med beskrivelsen i [RFC9293 afsnit 3.5](https://www.rfc-editor.org/rfc/rfc9293.pdf) og se om i kan se en sammenhæng? ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/wireshark_tcp.png)

    Her har vi fundet et three way handshake, fra vores kali vm via Proxmox
    ![Billede af Wireshark](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/ProxmoxVMWireshark.png)

5. Hvordan er tcp headeren opbygget? Brug jeres wireshark trafik og RFC9293 til at undersøge det.
![wireshark pakke](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/image.png)
![Billede fra RFC](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/Screenshot%202025-02-19%20125159.png)

6. Læs om [TLS handshake](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/)

7. Find et TLS handshake i jeres wireshark trafik og identificer `Client Hello`
![Image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/wireshark_tls.png) 
    - Hvor mange cipher suites understøtter klienten?
        ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/Screenshot%202025-02-19%20131149.png)
    - Hvilke TLS versioner understøtter klienten?
        Vi kan ikke finde understøttede versioner, men vi går ud fra, at det er TLSv1.2 fordi det er den, den er sendt med denne protokol
        ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/Screenshot%202025-02-19%20131925.png)

8. Identificer Server hello pakken.
![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/Screenshot%202025-02-19%20130532.png)
    - Hvilken cipher suite vælger serveren?
        ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/Screenshot%202025-02-19%20132150.png)
    - Hvilken TLS version vælger serveren?
        ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2013/Screenshot%202025-02-19%20132318.png)

9. Vi laver kort opsamling på klassen baseret på spørgsmål fra jer.
Jeg kigger på jeres gitlab dokumentation og giver feedback næste undervisningsgang.

## Ressourcer
Hvis i har brug for at genopfriske wireshark kan i bruge [THM: Wireshark: The Basics](https://tryhackme.com/room/wiresharkthebasics) eller [Wireshark docs](https://www.wireshark.org/docs/)