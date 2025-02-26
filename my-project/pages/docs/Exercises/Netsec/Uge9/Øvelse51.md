# Øvelse 51 - Netværksdesign med netværkssegmentering

## Information

Øvelsen er en gruppeøvelse.

I denne øvelse skal i arbejde med hvordan en typisk virksomhed kan højne sikkerheden ved at segmentere sit netværk.
Segmenteringen må gerne udføres logisk med VLAN's hvis det ønskes, men det kan måske være lettere at gøre med fysiske forbindelser hvis i ikke har så meget erfaring med VLANS.
Husk at placere firewalls relevante steder i netværket.
Udgangspunktet er at virksomheden har et fladt netværk, det vil sige at alle enheder befinder sig på det samme subnet

Virksomheden har ca. 300 ansatte i forskellige afdelinger, afdelingerne har forskellige funktioner, hardware og behandler forskellige typer af data, som bør indgå i jeres diskussion og segmenterings forslag.

Afdelingerne er:

**Teknologi og IT:**

- Netværksinfrastruktur: Ansvar for styring og administration af routere, switches og andre netværksenheder.
- On-premise servere: Hosting af applikationer, databaser og andre tjenester.

**Ledelse og Administration:**

- Topledelse: Strategiske planer, øverste ledelsesbeslutninger og følsomme interne oplysninger.
- HR (Human Resources): Indeholder personlige oplysninger, ansættelseskontrakter, løn og andre følsomme HR-data.
- Finans: Inkluderer økonomiske oplysninger, regnskaber og lønningsoplysninger.

**Operationelle Afdelinger:**

- Produktion: Produktionsdata og styring af produktionslinjer.
- Lager: Opbevaring af varer og lagerstyring.
- Leverandørkæde: Data relateret til leverandører og forsyningskædeprocesser.

## Instruktioner

1. I jeres gruppe skal i undersøge og diskutere, hvilke segmenter der bør være i netværket. Overvej faktorer som afdelingsopdeling, sikkerhedszoner, usikre enheder og behovet for at beskytte følsomme data.
Husk at bruge de links jeg har listet herunder, der er god inspiration til hvordan større netværk kan segmenteres.

    Topledelse skal være fuldt ud segmenteret

    Alt efter om on-prem skal eksponeres til internettet omhandler, hvorvidt man hoster ting, som skal tilgås.



2. Når i har identificeret de nødvendige segmenter, skal i tegne et netværksdiagram, der viser netværket. Inkludér som minimum routere, switche og firewalls. Meget gerne andre foranstaltninger hvis i kender til dem, som for eksempel Intrusion detection systemer.

    

3. Dokumenter jeres netværksdesign og et resume af gruppens overvejelser i jeres gitlab projekt. Husk at inkludere de kilder i har brugt i jeres overvejelser.

    ![img](../../../Images/ØvelsesBilleder/Netsec/Øvelse%2051/netvrksdiagram.drawio.png)

4. Vi tager en kort runde på klassen med udgangspunkt i en af gruppernes diagram når i er færdige med øvelsen. Alle grupper deltager i debat om løsningen.




## Ressourcer

- [Cloudflare - What is network segmentation?](https://www.cloudflare.com/learning/access-management/what-is-network-segmentation/)

- [OWASP Network segmentation Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Network_Segmentation_Cheat_Sheet.html)

- [sergiomarotco/Network-segmentation-cheat-sheet](https://github.com/sergiomarotco/Network-segmentation-cheat-sheet?tab=readme-ov-file)