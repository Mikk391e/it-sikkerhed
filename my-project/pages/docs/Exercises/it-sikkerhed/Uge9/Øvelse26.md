# Øvelse 26 - Wireshark analyse

##  Information

I denne øvelse skal du bruge wireshark til at analysere netværkstrafik fra et angreb.
Wireshark er en del af kali linux.
Trafikken er optaget i en `.pcap` fil som wireshark kan læse.

**Målet med øvelsen er at lære at bruge wireshark, altså at få brugt mulighederne i de forskellige menuer og undersøge hvordan man kan filtrere og analysere netværks trafik.**

Den specifikke pcap fil er ikke så relevant og spørgsmålene i instruktionerne er mest for at have noget at arbejde efter.
Det vil sige at du selv bestemmer hvor meget tid du bruger på den her øvelse, men du lærer mest ved at være nysgerrig, bruge dokumentation og selv lave søgninger på ting du ikke kender eller forstår i wireshark.

Øvelsen tager udgangspunkt i filen `malware-traffic-analysis.net-2014-12-15.zip` som du kan finde på itslearning i dagens plan. I zip filen finder du index.html som giver et overblik over de øvrige filer, blandt andet en fil med svar.
Der er også en ekstra .pdf fil som giver gode forklaringer: `2014-12-15-traffic-analysis-exercise-additional-information.pdf`

Inden du hopper til løsningen og den ekstra .pdf fil, så prøv at besvare alle spørgsmålene, dem du ikke kan besvare springer du bare over og gemmer til du ser løsningen.

Det er nok nødvendigt at bruge wireshark dokumentationen mens du arbejder, den er her:
https://www.wireshark.org/docs/wsug_html_chunked/

Der er også nogle wireshark tutorials her: https://www.malware-traffic-analysis.net/tutorials.html

## Instruktioner

1. Hent `malware-traffic-analysis.net-2014-12-15.zip` og pak filen ud (zip password er infected)

2. Udpak `.pcap filen` fra `2014-12-15-traffic-analysis-exercise.pcap.zip`

3. Åbn `.pcap` filen i wireshark

4. Indstil hvad du ser i wireshark https://unit42.paloaltonetworks.com/unit42-customizing-wireshark-changing-column-display/

5. Besvar følgende:
    * Hvad er hostnavne på de 3 windows maskiner i pcap filen ?

        ip: 192.168.204.139 - Host name = ROCKETMAN-PC - 00:0c:29:61:c1:89
        ip: 192.168.204.146 - Host name = WORKSTATION6 - 00:0c:29:fc:bc:2e 
        ip: 192.168.204.137 - Host name = MYHUMPS-PC - 00:0c:29:9d:b8:6d

    * Hvad er IP adressen/adresserne, på windows maskinen/maskinerne som er blevet ramt af et expolit kit ?
    
        Jeg ved ikke, om det er rigtigt, men hvis vi kigger efter alle http requests, og hvilke porte de bruger, vil vi kunne se, at alle requests bruger destinationsporten 80, undtagen nogle få stykker:
        ![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2026/Screenshot%202025-02-24%20125520.png)

    * Hvad er MAC adressen/adresserne, på windows maskinen/maskinerne som er blevet ramt af et expolit kit ?

        ip: 192.168.204.139 - Host name = ROCKETMAN-PC - 00:0c:29:61:c1:89
        ip: 192.168.204.146 - Host name = WORKSTATION6 - 00:0c:29:fc:bc:2e 
        ip: 192.168.204.137 - Host name = MYHUMPS-PC - 00:0c:29:9d:b8:6d
    
    * Hvad er navnet/navnene på domænet/domænerne på den/de kompromitterede hjemmeside/hjemmesider ?

        epzqy.ipheaba.eu
    
    * Hvad er IP adressen/adresserne, på den/de kompromitterede hjemmeside/hjemmesider ?
    
    * Hvad er navnet/navnene på domænet/domænerne på exploit kittet (måske flere ?) ?
    
    * Hvad er IP adressen/adresserne, på exploit kittet (måske flere ?) ?
    
    * Er der nogen af windows maskinerne der er blevet inficeret, hvis ja hvilke ?
    
    * Hvilket/hvilke exploit kit(s) er nævnt i pcap filen ?
    
    * Hvilken exploit er anvendt ved hjælp af expolit kittet/kitne ? (Flash, Java, IE, etc)
    
    * Hvilken URL(s) er anvendt som redirect mellem den/de kompromitterede hjemmeside(r) og exploit kittet/kitne ?
    
    * Hvad er ip redirect adressen/adresserne på redirect URL(s) ?

6. kontroller dine svar i forhold til øvelsens svar og ekstra information som du kan finde i `malware-traffic-analysis.net-2014-12-15.zip`

## Links

Hvis du betaler for tryhackme, er der et godt rum til at lære om wireshark analyse https://tryhackme.com/room/wiresharkpacketoperations