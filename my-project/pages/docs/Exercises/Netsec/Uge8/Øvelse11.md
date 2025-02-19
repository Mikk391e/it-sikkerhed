# Øvelse 11 - OSI modellen og enheder

### Information
OSI modellen har 7 lag og er en referencemodel for hvordan systemer kommunikerer.
Modellen er grundlæggende i arbejdet med netværk og netværkssikkerhed.

Dette er en gruppeøvelse.

Formålet med øvelsen er at i danner jer et overbik over modellen og hvilke enheder der hører til på hvilke lag i modellen.
At vide hvilke enheder der arbejder på hvilke lag i modellen er grundlæggende for at forstå hvordan de enkelte enheder kan være sårbare samt hvilke enheder der kan indsættes som foranstaltning.
Der er for eksempel forskel på en firewall der filtrerer ip adresser, hvilket kan siges at være på lag 3 (netværkslaget) og en der inspicerer data hvilket kan siges at være på lag 7 (applikationslaget).
Segmentering af netværk hører også sammen med OSI modellen hvor f.eks VLAN's foregår på lag 2 ting og routing sker på lag 3.
Endelig er OSI modellen er værktøj til at udføre fejlfinding. Hvis du for eksempel kan pinge en enhed, hvilket bruger [ICMP](https://www.rfc-editor.org/rfc/rfc792) protokollen på lag 3 kan det bruges til at udelukke fejl på lag 1 og 2.

![image](../../../Images/ØvelsesBilleder/original-seven-layers-of-osi-model.png)

kilde: https://community.fs.com/article/tcpip-vs-osi-whats-the-difference-between-the-two-models.html

## Instruktioner

1. Gennemfør i fællesskab tryhackme rummet [OSI model](https://tryhackme.com/room/osimodelzi)
![alt image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2011/Screenshot%202025-02-19%20095419.png)
![alt image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2011/Screenshot%202025-02-19%20095507.png)
![alt image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2011/Screenshot%202025-02-19%20095652.png)
![alt image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2011/Screenshot%202025-02-19%20095838.png)
![alt image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2011/Screenshot%202025-02-19%20095936.png)
![alt image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2011/Screenshot%202025-02-19%20100102.png)
![alt image](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2011/Screenshot%202025-02-19%20100144.png)

2. Find almindelige (consumer) eksempler på hardware enheder, og placer dem på OSI modellen.
    
    [Cisco Catalyst 9200L](https://www.proshop.dk/Switch/Cisco-Catalyst-9200L/3139718) : Data Link laget - Layer 2

    [Oral-B Eltandbørste iO9 Duo Black Onyx](https://www.proshop.dk/Eltandboerste/Oral-B-Eltandboerste-iO9-Duo-Black-Onyx-Rose-Quartz/3268077)  : Data Link laget - Layer 2

3. Find nye/sjældne/esoteriske enheder (fysiske eller virtuelle) (med referencer) - f.eks. next-gen firewalls, proxies, application gateways. Hvad-som-helst med et netstik/wifi er ok at have med.

    Placeholder

4. Lav en oversigt der tydeligt viser hvilke enheder i har fundet og hvilket lag i OSI modellen de hører til, inkluder det i jeres gruppes gitlab dokumentation.

    Placeholder

5. Vi laver kort opsamling på klassen baseret på spørgsmål fra jer.
Jeg kigger på jeres dokumentation og giver feedback næste undervisningsgang.

    Placeholder

## Ressourcer

Links om OSI modellen se:

- https://www.itu.int/rec/T-REC-X.200-199407-I
- [comparitech](https://www.comparitech.com/net-admin/osi-model-explained/)
- [techterms](https://www.youtube.com/watch?v=vv4y_uOneC0)