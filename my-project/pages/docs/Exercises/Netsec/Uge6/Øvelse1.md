# Øvelse 1 - Genopfriskning af grundlæggende netværk

### **Hvad er internettet?**

Mange forbundne enheder - IoT (internet of things) devices. 

Packet switches - sender data packets

Communication links - fiber, kobber, radio, satellit 

Internettet er et netværk af netværk

Internettet kan ses som en service i form af streaming, tilgang til internettet, videospil

Protokoller:
En protokol definere formatet, rækkefølgen af sendte og modtagne beskeder imellem netværksenheder og handlinger ved besked transmission og modtagelse

### Network Edge

Kabel baseret netværk - forskellige husholdninger har hver deres frekvens, ligesom radiokanaler. Her bruges FDM (frequency division multiplexing)

Kablede forbindelser er asymmetriske forstået på den måde, at ens downstream er højere en ens upstream 

DSL (digital subscriber line) er internet gennem telefonstik

Distancing til leverandøren har betydning for hastigheden af netværket

Packet transmisison delay:

tiden det tager at sende L-bit packet i en forbindelse = L (bits) / R (bits/sec)

### Network Core

2 nøglefunktioner:

Forwarding:
Sker lokalt
Pakcets har en destination i deres header, hvorefter routeren sender pakken det rigtige sted hen via dens routing table

Routing:
Routing er en global aktion
Hvordan kommer pakken fra afsenderen til modtageren

Queueing sker, når mængden af pakker, som bliver sent på en gang, er for stor til at blive håndteret på samme tid

Det er også i denne forbindelse der opstår packet loss, da routerens hukommelse kan være udtømt, så der ikke er plads til pakken i hukommelsen.

Ovenstående kaldes for packet switching

Circuit switching er et kald fra kilden til destinationen, hvor alle ressourcer er allokeret til denne forbindelse

### Performance

Performance bottlenecks er ofte i network edge

Forskellige former for delay - propagation delay er distancen, som data sendes over. Så f.eks. fra USA til Europa

### Layering, Encapsulation

OSI model: (Please Do Not Throw Sausage Pizza Away)

Application - HTTP, IMAP, POP3, SMTP, DNS            Besked

Presentation 

Session

Transport - TCP, UDP                        |  Segment           Besked og transportheader

Network - IP, routing protokoller  |  Datagram         Besked, transportheader og netværksheader

Data Link - Ethernet, WiFi, PPP       |  Frame

Physical - bits “on the wire”