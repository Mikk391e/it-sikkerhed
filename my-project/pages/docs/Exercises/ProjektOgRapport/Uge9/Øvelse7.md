## Øvelse 7: Empiri & Data

### Information
Formålet med denne øvelse, er at introducere begreberne _Empiri_ samt _Data_ og vise begrebernes relationer til tidligere emner i faget. 

### Empiri & Vidensgrundlag
I den _Akademiske_ verden tales der ofte om _empiri_, hvilket er defineret som følgende i den [danske ordbog](https://ordnet.dk/ddo/ordbog?query=empiri): _"erfaringer og iagttagelser anvendt som grundlag for (videnskabelig) erkendelse"_ 
  
I den akademiske verden refererer "empiri" til de erfaringer og observationer, som bruges til at underbygge videnskabelige påstande, ofte gennem systematisk indsamling af data (f.eks. eksperimenter, observationer, interviews, undersøgelser).  
Formålet er at skabe et objektivt og pålideligt grundlag for erkendelse.

I dagligdags tale kan "empiri" forstås som de data eller beviser, der understøtter en påstand og dermed styrker dens validitet og integritet.  
Den empiri man anvender til at understøtte et projekts validitet og integritet, kaldes det empiriske grundlag.
  
Groft sagt kan man dele et projekts empiriske grundlag op i to:  
  
  - Den empiri vi indhenter fra andre gennem vores vidensgrundlag [(Se opgave 5 - Vidensgrundlag)](../exercises/5_Vidensgrundlag.md)
  - Den empiri vi selv skaber gennem eksperimenter (f.eks. test), observationer (f.eks. analyse af log filer) og undersøgelser (f.eks. interviews etc.)  

Et projekts anvendte empiri baseres på data, som er indsamlet og analyseret med det formål, at validere og understøtte de påstande, der fremsættes.  
At arbejde med empiri kræver derfor ikke kun en forståelse af de metoder, der anvendes til at indsamle data, men også en kritisk tilgang til, hvordan data analyseres og tolkes.  
I sidste ende er både empiri og data fundamentale byggesten for at skabe pålidelige og valide  resultater og det er vigtigt at være opmærksom på, hvordan de anvendes i projektet.

### Data der anvendes i projekter

I projekter anvendes der to typer data:  
  
- Kvantitativ data
- Kvalitativ data

Kvantitativ data er målbart (kvantitativ analyse), hvorimod kvalitativ data ofte skal fortolkes (kvalitativ analyse).  
Data indsamles altid ud fra en beskrevet metode, hvor kvalitative metoder er gode til at undersøge kontekster og adfærd, mens kvantitative metoder er gode til at undersøge mønstre og tendenser.

#### Kvantitativ data

Kvantitativ data er data, der kan måles og kvantificeres i tal. Denne type data bruges ofte til at identificere mønstre, tendenser og sammenhænge på baggrund af store mængder talmateriale.  

Eksempler på kvantitativ data i IT-sikkerhed:  
  
- **Antal sikkerhedsbrud**: Hvor mange gange har en given organisation oplevet et cyberangreb i løbet af det seneste år?
- **Antal sårbarheder opdaget i et system**: Hvor mange kendte sårbarheder (CVEs) er blevet opdaget i et IT-system inden for de sidste 6 måneder?
- **Procentdel af systemer opdateret**: Hvad er procentdelen af systemer, der er blevet opdateret med de nyeste sikkerhedsopdateringer?
- **Firewall-trafiklogfiler**: Antal blokeringer af uautoriseret trafik pr. måned i en firewall.

Et konkret eksempel på anvendelse af kvantitativ data i IT-sikkerhed kunne være en analyse af tidsforbruget på håndtering af falske positive alarmer i et _Security Operations Center_ (SOC).  
Hvis en organisation har en mistanke om, at medarbejdere bruger for meget tid på at håndtere falske alarmer, kan kvantitativ data anvendes til at identificere og dokumentere tidsforbruget, ved hjælp af en systematisk metode.

**Metodevalg**:  
For at undersøge medarbejdernes tidsforbrug på håndtering af falske positive alarmer, kan en **observationsmetode** anvendes. Metoden involverer, at man observerer og registrerer, hvordan medarbejderne håndterer alarmer over en bestemt periode, f.eks. en uge.  
Her bliver data indsamlet ved at notere, hvor lang tid hver medarbejder bruger på at analysere og håndtere hver falsk alarm.  

Dette kan gøres ved at oprette en **logbog**, hvor medarbejdernes tidsforbrug bliver registreret for hver alarm. På den måde får man et konkret datasæt, der kan analyseres statistisk, f.eks. ved at beregne gennemsnitligt tidsforbrug pr. alarm.  
Hvis en medarbejder bruger 10 minutter på at håndtere én alarm og 30 minutter på en anden, kan dette data bruges til at identificere mønstre eller flaskehalse i processen.
  
Ved at anvende denne **metodiske tilgang** til at indsamle kvantitativ data, får organisationen et målbart grundlag, der kan bruges til at analysere arbejdsprocesserne, og vurdere om der er behov for forbedringer.  
Anvendelsen af en systematisk metode sikrer, at dataen er pålidelig og kan bruges til at træffe informerede beslutninger om, hvordan man optimerer ressourcerne i SOC.
  
**_Bonusinformation_**:  
Hvis der ikke allerede findes kvantitativ data om tidsforbruget, kan dette problem adresseres i problemformuleringen, f.eks. ved at inkludere et underspørgsmål som:  
- "Hvor meget tid anvender medarbejderne i SOC på håndtering af falske positive alarmer?" 
Dette gør det muligt at definere præcist, hvad der skal måles og hvordan dataene skal indsamles ved hjælp af den valgte metode.
  
#### Kvalitativ data

Kvalitativ data består af ikke-målbare data, som f.eks. beskrivelser, observationer eller interviews. Denne type data bruges til at opnå en dybere forståelse af kontekster, adfærd eller mønstre, som ikke kan indfanges ved hjælp af kvantitativ data.  
I IT-sikkerhed kan kvalitativ data hjælpe med at forstå de menneskelige faktorer, der påvirker sikkerhedsforanstaltninger eller de organisatoriske kulturer omkring cybersikkerhed.

Eksempler på kvalitativ data i IT-sikkerhed:  
  
- **Brugerfeedback på sikkerhedsforanstaltninger**: Hvilke udfordringer oplever brugere, når de bruger multi-faktor autentificering? Hvordan beskriver de deres oplevelser og bekymringer?
- **Interviews med IT-sikkerhedspersonale**: Hvad mener IT-sikkerhedspersonalet om de nuværende sikkerhedsforanstaltninger i organisationen? Hvilke forbedringer foreslår de?
- **Observation af medarbejderes adfærd**: Hvordan håndterer medarbejdere sikkerhedsprotokoller, som f.eks. password-håndtering eller sikring af mobile enheder? Hvad kan observeres, der tyder på manglende overholdelse af sikkerhedspolitikker?
- **Fokusgrupper om cybersikkerhedskultur**: Hvordan oplever medarbejdere virksomhedens cybersikkerhedspolitikker og procedurer? Hvordan vurderer de organisationens samlede sikkerhedskultur?

Et konkret eksempel på kvalitativ data i IT-sikkerhed, kan være en undersøgelse af medarbejdernes opfattelse af virksomhedens cybersikkerhedspolitikker, samt deres erfaringer med at følge sikkerhedsvejledninger.

**Metodevalg**:  
For at indsamle kvalitativ data om medarbejdernes opfattelse og erfaringer med cybersikkerhed kan man anvende **semi-strukturerede interviews**.  
I denne metode interviewer man et udvalg af medarbejdere, hvor spørgsmålene er åbne og giver mulighed for dybdegående svar.  
For eksempel kunne et spørgsmål være: "Hvordan oplever du, at de nuværende sikkerhedsforanstaltninger påvirker din daglige arbejdsrutine?" 

**Metodebeskrivelse**:  
  
- Interviewene bliver transskriberet og de indsamlede svar analyseres ved hjælp af **kvalitativ dataanalyse**, som f.eks. **tema-analyse**.  I denne type analyse identificerer man de vigtigste temaer og mønstre i medarbejdernes svar, som kan give indsigt i deres opfattelser af virksomhedens sikkerhedskultur og hvilke udfordringer, de støder på.
- Efter transskription og tematisk analyse kan man få indsigt i, hvor medarbejderne oplever, at sikkerhedsforanstaltningerne er ineffektive eller uhensigtsmæssige. Det kan også afsløre, hvordan medarbejderne opfatter organisationens engagement i cybersikkerhed og hvad der kan gøres for at forbedre adfærden.

**Eksempel på anvendelse**:  
Forestil dig en situation, hvor en organisation har implementeret en ny politik for opbevaring og håndtering af følsomme personoplysninger (f.eks. kreditkortinformationer eller personlige identifikationsnumre).  
Organisationen opdager, at der er udfordringer med medarbejdernes forståelse af politikken og dens praktiske anvendelse.  
Ved at gennemføre interviews kan man indsamle **kvalitativ data** der gør det muligt at forsta hvorfor medarbejderne ikke overholder politikken eller om de er usikre på, hvordan de korrekt opbevarer og beskytter de følsomme personoplysninger.

Måske viser interviewene, at medarbejderne er usikre på, hvilke systemer der er sikre at bruge til opbevaring af følsomme personoplysninger, eller måske er de ikke opmærksomme på de risici, der er forbundet med manglende overholdelse af politikken.  
Gennem interviewene får organisationen en bedre forståelse af de udfordringer, medarbejderne møder, og hvordan de kan forbedre opbevaringspraksis og træning for at sikre, at følsomme personoplysninger bliver korrekt håndteret og opbevaret.

Denne kvalitative tilgang kan hjælpe organisationen med at identificere de specifikke problemer, der hæmmer overholdelse af sikkerhedspolitikkerne, og muliggøre målrettede forbedringer i uddannelse, processer og systemer for bedre at beskytte personfølsomme oplysninger.

Ved at anvende kvalitative metoder kan organisationen få en dybere forståelse af de menneskelige faktorer, der påvirker cybersikkerheden samt etablere tiltag til at ændre processer eller sikkerhedsforanstaltninger for at sikre bedre compliance og en stærkere sikkerhedskultur.
  
#### Datagrundlag
  
Når man arbejder med data, er det essentielt at forstå datagrundlaget – den samling af data, som en analyse eller undersøgelse bygger på.  
Datagrundlaget danner fundamentet for de konklusioner, der drages, og dets kvalitet er afgørende for pålideligheden af resultaterne.  
Man kan tale om et **stærkt datagrundlag** eller et **svagt datagrundlag**, afhængigt af, hvordan dataene er indsamlet og repræsenterer den virkelighed, der undersøges.

**Eksempel på svagt datagrundlag:**:  
Hvis man ønsker at afdække, hvilket fag på Pba. IT-sikkerhed flest studerende føler sig udfordret i og kun spørger én ud af 30 studerende, der svarer "Projekt & rapport", vil konklusionen bygge på et **svagt datagrundlag**.  
Den ene studerende er ikke repræsentativ for de øvrige, og derfor er konklusionen usikker.

**Eksempel på stærkt datagrundlag:**:  
Hvis 15 ud af de 30 studerende svarer det samme, begynder man at tale om en **tendens** og datagrundlaget er mindre svagt.  
Hvis alle 30 studerende svarer "Projekt & rapport", er der tale om et **stærkt datagrundlag**, hvor konklusionen er meget pålidelig.

**Betydningen af Datagrundlagets Kvalitet**:  

Det er ikke kun i empirisk datainsamling, at datagrundlaget er vigtigt. Også når vi anvender eksisterende forskning i vores vidensgrundlag, skal vi være opmærksomme på datagrundlaget for den forskning.  
En vigtig del af kildekritik er at vurdere, hvilket datagrundlag en given undersøgelse bygger på. Her er nogle faktorer, man bør overveje:

- **Repræsentativitet:**  
Er dataene repræsentative for den population eller situation, der undersøges? F.eks. kan resultaterne fra en undersøgelse, der kun inddrager én sektor eller region, ikke nødvendigvis generaliseres til andre.
  
- **Størrelse:**: 
Er datagrundlaget stort nok til at kunne drage pålidelige konklusioner? Små prøvestørrelser kan give et skævt billede af virkeligheden.

- **Kontekst:**: 
 Hvordan blev dataene indsamlet og i hvilken kontekst blev de indsamlet? Er der nogen biases (forudindtagelser) i dataindsamlingen?  
 Det er vigtigt at forstå, hvordan data er blevet indsamlet, så vi kan vurdere, om de afspejler det fænomen det ønskes at forstå.

**Eksempel på kontekstafhængighed af datagrundlag:**:  
En relevant case er anvendelsen af _OWASP Top 10_, som er en liste over de 10 mest kritiske sikkerhedsrisici for webapplikationer. OWASP baserer sin liste på data indsamlet fra virksomheder, der frivilligt deler deres data. Relevansen af OWASP Top 10 afhænger derfor af, hvilke typer af virksomheder der bidrager med deres data. Hvis majoriteten af de indsamlede data stammer fra virksomheder i USA inden for banksektoren, vil det måske ikke være lige så relevant for et projekt, der omhandler cybersikkerhed i et hospital, hvor der kan være andre typer af sårbarheder.  
Her vil man så være nød til at enten kigge i den rå data som _OWASP_ basere sin top 10 på, for at vurdere om lige netop den data også er relevant.
  
Omvendt kan man sige at man med Mitre ATT&CK databasen, relativt nemt kan afgøre om data passer til lige netop ens egen kontekst, da man kan se hvilken industrier _Advanced persisten threats_(APT) målretter sig imod,
samt hvilken geografiske dele af verden, de er mest aktive i. Altså Mitre ATT&CK tilbyder mere præcis data, og relevansen af denne ift. eget projekt, kan derfor nemmere vurderes.

**Validitet og Kildekritik**:  

Når man arbejder med eksternt indsamlede data, f.eks. gennem forskning eller rapporter, er det afgørende at vurdere validiteten af datagrundlaget. **Validitet** handler om, hvor godt dataene afspejler den virkelighed, de er ment at måle.  
Hvis dataene ikke er valide, kan de føre til fejlagtige konklusioner.

Derudover er **kildekritik** et væsentligt element i evalueringen af datagrundlaget. Det er vigtigt at overveje:
- Hvem har indsamlet dataene?
- Hvilke metoder blev brugt?
- Er der nogen interesser, der kan have påvirket dataindsamlingen eller rapporteringen?

**Datagrundlagets Opløsning**:  
  
En anden vigtig dimension af datagrundlaget er dets **opløsning**, som refererer til detaljeringen og præcisionen af de data, der er blevet indsamlet. Dette omfatter faktorer som:

- **Tidsopløsning:** Hvor ofte er dataene blevet målt? Er det på dagligt, månedligt eller årligt niveau? Tidsopløsning har en stor betydning for, hvor præcist vi kan analysere tendenser over tid.
  
- **Rumlig opløsning:** Hvis data er geografisk opdelt, er det vigtigt at vurdere, hvor præcist disse geografiske data er målt. For eksempel kan data om IT-sikkerhedsbrud i én region ikke nødvendigvis være repræsentative for en hel nation.

**Opsummering - datagrundlag**:

Datagrundlaget er en central faktor for, hvordan data kan anvendes i forskning og projekter. Det er vigtigt at vurdere både kvaliteten og relevansen af det data, man arbejder med, for at sikre, at de konklusioner, man drager, er pålidelige og valide. Vær altid opmærksom på datagrundlagets størrelse, repræsentativitet og kontekst for at sikre, at de anvendte data kan underbygge de nødvendige beslutninger.


### Opsummering
Du er blevet introduceret til flere nye begreber. Du er introduceret til begrebet empiri som indhentes fra et videngrundlag. Empirien kan F.eks. være en artikel som indeholder noget data.
Data'en kan enten være kvantativ, eller kvalitativ. Nøjagtigheden af den data der anvendes, vurderes udfra datagrundlaget.
  
#### Kvalitets kriterier  
Dataens pålidelighed og kildekritik er fundamentale elementer, der sikrer, at de anvendte data er både valide og pålidelige.  
   
- **Validitet**:  
Det er vigtigt at vurdere, om de målte data afspejler det, de er ment at måle. For eksempel, når man måler hændelsehåndtering i IT-sikkerhed, skal man sikre sig, at de målte hændelser er relevante og præcise.  
- **Pålidelighed**:  
Når man anvender andres målinger, er det nødvendigt at vurdere kilden kritisk, især hvis formålet med målingen kan være kommercielt eller biased, som eksempelvis i markedsføringskontekster.

Når data anvendes i analysen, skal det overvejes, om det er korrekt anvendt til at besvare de oprindelige spørgsmål:  
  
- **Hvor meget-spørgsmål**:  
(typisk kvantitative data) giver præcise, numerisk målbare svar, f.eks. på hvor mange hændelser, der opstår i en given periode. Kvantitative data er ofte mere nøjagtige og giver lette sammenligningsgrundlag.  
- **Hvordan og hvorfor spørgsmål**:  
(typisk kvalitative data) giver en dybere forståelse af baggrund, kontekst og nuancer, som kan være nødvendige for at forstå årsagerne til hændelser eller problemstillinger.

#### Data behov  
For at udlede de nødvendige data til et projekt er det afgørende at identificere, hvilken type data der er påkrævet i de forskellige faser af projektet. Dette kan omfatte data indsamlet gennem litteratur, observationer, interviews eller endda detektivarbejde i organisationen, hvor man afdækker, hvilke dele der eksisterer, og hvordan de fungerer.  

I et projekt, hvor målet f.eks. er at "øge med 5%", vil databehovet være at forstå, hvad en 5% øgning konkret betyder. Hvilket udgangspunkt er der, og hvordan måles fremgangen? Hvilke baseline-data er nødvendige for at kunne vurdere denne ændring?

Når man arbejder med projekter, der har til formål at forbedre noget eksisterende – som ofte er tilfældet i IT-sikkerhedsprojekter – vil analysen typisk involvere dataindsamling, herunder årsagsanalyse og evaluering af eksisterende processer og systemer:  
  
- **Problemanalyse og dataindsamling**:  
Her indsamles data, som kan belyse årsagerne til de udfordringer, der skal løses.  
  - Eksempler på metoder til dette kan være GRC (Governance, Risk Management, Compliance) gap-analyser, hvor man undersøger hvilke områder i organisationens systemer, der ikke lever op til de ønskede standarder.
  - **Pentesting af systemer** for at identificere sårbarheder og fejl i IT-sikkerheden.
  - **Tidsforbrug på sikkerhedsrelaterede opgaver** for at forstå, hvor meget ressourcer der bruges, og hvordan man kan optimere processerne.

Databehovet skal også afklares i forhold til gældende standarder og bedste praksis, hvilket kan være en vigtig del af behovsafklaringen.
  
### Instruktioner

**De rapporter som anvendes i trin 1 & 2 herunder, kan findes [i dette Repository](https://github.com/jacobdjwilson/awesome-annual-security-reports)**

1. Inde i repositoriet med sikkerhedsrapporter skal I finde den rapport, der hedder _Microsoft Digital Defense Report_, og vurdere samt redegøre for følgende: 
  
      - **Præsenteres der primært kvantitativ eller kvalitativ data i rapporten?**

        Det er primært kvantitative data. Rigtige mange målbare data
   
      - **Hvorfor anvendes der primært denne datatype (kvantitativ eller kvalitativ)?**

        Dataen er automatiseret og kommer fra Microsoft systemer, hvor der ikke er menneskelig interaktion. Det er sådan nogle ting som audit logs.

      - **Hvilke faktorer gør rapporten troværdig?**
   
        Afsenderen. Microsoft er dominerende inden for IT. Kæmpe autoritet.

      - **Hvilke faktorer gør rapporten utroværdig?**

        Mulighed for partiskhed, ved at det er Microsoft, som oplyser deres egne tal. Muligvis interesse i at bruge det som salgstale.
        Svært at faktatjekke, da der gøres brug af interne data.
   
      - **Hvornår kan lige netop denne rapport indgå i et projekts empiriske grundlag?(Hvilken kontekst?)**

        Analyse trusselsbillede, trusselsvurdering. Også i forhold til den pågældende trussel mod en given sektor. 

2. Inde i repositoriet med sikkerhedsrapporter skal I finde den rapport, der hedder _CompTIA State of Cybersecurity 2025_, og vurdere samt redegøre for følgende:
  
      - **Hvilken metode er anvendt til at skabe det empiriske grundlag for denne rapport?**
   
        En kvantitativ spørgeskemaundersøgelse

      - **Hvis der tages udgangspunkt i den geografiske placering af de virksomheders besvarelser, som datagrundlaget er skabt ud fra, kan dataene så være relevante for en dansk virksomhed? Husk at argumentere. Hvorfor? / Hvorfor ikke?**
   
        Hvorfor:

        - Inden for IT, er der en "best practice", som ikke nødvendigvis ændrer sig på tværs af landegrænser.

        Hvorfor ikke:
        
        - Mulgivis forskelle i kultur, som smitter af på, hvordan man tænker cybersikkerhed. Der er måske forskelle i virksomhedsstruktur, som ikke er ligeså relevant for danske virksomheder.

      - **Er rapporten en troværdig kilde?**

        De arbejder sammen med NIST, som er anerkendt, så det taler for. Det taler meget for, at de er en non-profit organisation.
   
3. Forrige lektion læste I forskningsartiklen _"Good" Organizational Reasons for "Bad" Cybersecurity_. I skal vurdere og redegøre for følgende:

      - **Præsenteres der primært kvantitativ eller kvalitativ data?**

        Kvalitativ data. Observation samt en form for interview.
   
      - **Hvorfor anvendes der primært den type data?**

        En faktor er, at SMV'er ofte ikke har hård data over, hvordan deres it-sikkerhed er.

        Fordi naturen af observationer gør, at man ser folks procedure og processer.

### Links
- [ordnet.dk - Empiri](https://ordnet.dk/ddo/ordbog?query=empiri)
- [ordnet.dk - Data](https://ordnet.dk/ddo/ordbog?query=data)
- [ordnet.dk - Grundlag](https://ordnet.dk/ddo/ordbog?query=grundlag)
- [ordnet.dk - Kvalitativ](https://ordnet.dk/ddo/ordbog?query=kvalitativ)
- [ordnet.dk - Kvantitativ](https://ordnet.dk/ddo/ordbog?query=kvantitativ)
- [Repository med link til årlige sikkerheds rapporter - Github](https://github.com/jacobdjwilson/awesome-annual-security-reports)