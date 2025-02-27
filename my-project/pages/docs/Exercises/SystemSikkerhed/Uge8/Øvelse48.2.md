**Undersøg Mitre ATT&CK taktikken TA0004 – Privilege Escalation.**

- Hvad betyder denne taktik, og hvordan bruges den i angriberens proces? Hvorfor er den et vigtigt mål for angribere?

Svar: Når man har fået adgang til et system, går mand efter at få mere adgang. Efter man er kommet ind i et system er det typisk med en bruger der ikke har så mange rettigheder og mand bruger derfor privilege escalation til at få flere rettigheder og udføre sit egentlige angreb.

Ransomware skal brug adgang til at ændre. Dette kan skaffes privilege escalation.

---

**Identificer specifikke under-teknikker under T1548.**

- Undersøg de underliggende teknikker under T1548, som er relateret
til Privilege Escalation. Hvordan bidrager disse teknikker til
angriberens evne til at opnå Privilege Escalation?

Svar: Fra en bruger med lave rettigheder på et system, kan man via misbrug af kontrol mekanismer (”run as admin”), eksekvere kode på systemet med højere rettigheder end den indfiltrede bruger. 

- Beskriv konkrete eksempler på, hvordan teknikkerne under T1548 fungerer i praksis.

Svar:

001 - Setuid og setgid, ændring på setuid og setgid bits i en applikation så den kører i en anden brugers kontekst med flere rettigheder.

004 - levated Execution with Prompt: En trusselsaktør udnytter en mekanisme ved `AuthorizationExecuteWithPrivileges` API’en, hvor den ikke tjekker på om programmet, som beder om at eksekvere med root privilegier er et “anderkendt” program, som man kan stole på. Så alt trusselsaktøren skal, er at indtaste kodeordet når h*n bliver bedt om det.

002 - Bypass User Account Control: Kører et program som admin og sige “ja” til prompten eller indtaste et password UAC, prompt som når man prøver at kører en applikation som admin.

003 - Sudo Caching: Ændring at sudo fil i hukommelsen så der ikke skal bruges password i x antal tid. Passwordet gemmes i cach så det ikke skal skrives hver gang.

005 - Temp Elevated Cloud Access: Admin brugere på cloud har mulighed for at give tilladelse til at services eller brugere kan anmode om midlertidige eskalering af deres rettigheder. Dette kan udnyttes.  

006 -  TCC Manupulation: TCC Transparency Consent Control er en macOS kontrol mechanisme der kontrollere om en process har rettigheder til at tilgå services og data beskyttet af TCC som, mikrofon, kamera og Full Disk Access (FDA). TCC kan udnyttes for at skabe forhøjet eksekverings rettigheder.

---

**Identificer og undersøg Mitigeringen M1026.**

https://attack.mitre.org/mitigations/M1026/

- Hvad er formålet med **Mitigeringen M1026**?

Svar: Håndtere oprettelse, ændring, brug og rettigheder forbundet med privileged accounts. Dette inkludere SYSTEM og root.

- Hvordan hjælper denne mitigering med at forhindre eller begrænse Privilege Escalation?

Svar: Begrænsning af rettigheder via sudo passwords med timestamps på 0, så der altid skal skrives password hver gang der eksekveres kommandoer med højere rettigheder.

Begræns mulighed for at oprette brugere med høje rettigheder.

---

**Identificer og undersøg Detekteringen DS0022.**

- Hvad er **Detekteringen DS0022**, og hvordan anvendes den til at opdage aktiviteter relateret til Privilege Escalation?

Svar: Fil oplysninger/metadata kan bruges til at se mærkelig aktivitet. Det kan være ændringer på rettigheder.

- Diskuter metoder og værktøjer, der kan bruges til at implementere detekteringen i et system.

Svar: Logs, anti-virus (Microsoft defender), fil signatur (hash signatur).

---

**Præsentation af resultater:**

Forbered en kort præsentation, der opsummerer jeres resultater og diskussioner. Præsentationen skal indeholde:

- En forklaring på **Privilege Escalation-taktikken (TA0004)** og hvorfor den er vigtig.
- En oversigt over teknikkerne under **T1548** og hvordan de relaterer sig til Privilege Escalation.
- En gennemgang af **Mitigeringen M1026** og hvordan den kan implementeres.
- En beskrivelse af **Detekteringen DS0022** og dens anvendelse til at opdage angreb.

**Præsentationen skal være kort og præcis (maks. 5 minutter). Fokusér på at opsummere jeres fund i jeres præsentation.**