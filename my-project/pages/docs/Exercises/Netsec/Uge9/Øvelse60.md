# Øvelse 60 - Viden om firewalls

## Information

Øvelsen er en gruppeøvelse.

Firewalls er afgørende sikkerhedsenheder, der anvendes til at filtrere og kontrollere trafik mellem et internt netværk og det eksterne internet eller mellem forskellige segmenter af et netværk.
Der findes forskellige typer af firewalls, og de kan filtrere trafik på forskellige måder. I denne øvelse skal i undersøge forskellige typer af firewalls, hvad de er i stand til og hvilke svagheder de har.

Jeg har givet et par links herunder som inspiration, men i bør selv finde yderligere ressourcer som i kan bruge til at begrunde jeres undersøgelser. Husk at være kildekritiske!

## Instruktioner

1. I jeres gruppe skal i undersøge forskellige firewall typer og hvad de kan. De forskellige typer kan være:
    - Pakkefiltreringsfirewall
        - Denne firewall filtrerer udefrakommende pakker, som den opstiller mod nogle konfigurationer angående tilladte Ip-addresser, pakke type, port nummer, og andre dele ved protokol headeren.
        - Layer 3-4
        - svagheder:
            - Er sårbar over for ip-spoofing
            - Access control list kan være svær at sætte op og vedligeholde

    - Stateful Inspection Firewall
        - Udover bare at filtrere pakker, så kigger den også på, hvorvidt pakkerne er en del af en allerede etableret forbindelse. Den kigger også på payloaden
        - Layer 3-5
        - svagheder:
            - Ressourcekrævende
            - Er sårbar over for ip-spoofing, da den ikke validerer afsenderen

    - Application Layer Firewall (Proxy Firewalls)
        - Der er to former for Application Layer Firewall - aktiv og passiv.
        Den aktive inspicerer alle requests og deres payload. Kun hvis requesten er "clean", bliver den sendt videre.
        Den passive fungerer som et IDS, hvor den ikke dropper requests, men derimod giver en warning el. lign. Al trafik, både indgående og udgående, kommer igennem denne firewall
        - Layer 3-7
        - svagheder:
            - Ressourcekrævende, kan skabe en bottleneck
            - Det koster flere penge
            - Er ikke kompatibel med alle netværksprotokoller

    - Next-Generation Firewall (NGFW)
        - Så den gøre det samme som alle de andre, men den gør også brug af deep packet inspection.
        - Layer 3-7
        - svagheder:
            - For at få maksimal udbytte af denne firewall, skal den integreres med alle ens andre sikkerhedssystemer, hvilket kan være en meget kompliceret proces.
            - Den er dyr

    - Proxy Server Firewall (f.eks Web Application Firewall)
        - Denne firewall bruges til at sikre sikker http forbindelse mellem en web applikation og internettet. Denne fungerer som en reverse-proxy, da al trafik kommer igennem den, inden den rammer web applikationen.
        - Layer 7
        - svagheder:
            - Http smuggling - man skal sikrer sig, at både ens proxy og server bruger samme header (Transfer encoding: chunked, Content.length) eller bruger http/3

2. Lav en kort beskrivelse af hvad de forskellige typer kan, hvilket lag i OSI modellen de arbejder på og hvad deres svagheder er (hvordan de kan kompromitteres ved f.eks ip spoofing)
    


3. Dokumenter jeres undersøgelse og svar i jeres gruppes gitlab projekt, jeg giver feedback næste gang. Hvis vi har tid så tager vi en kort runde på klassen baseret på jeres spørgsmål.



## Ressourcer

- [Netwrix - [...]Common Types of Network Security Devices[...]](https://blog.netwrix.com/2019/01/22/network-security-devices-you-need-to-know-about/)
- [techtarget - 5 different types of firewalls explained](https://www.techtarget.com/searchsecurity/feature/The-five-different-types-of-firewalls)