# Opgave 10 - Brugerrettigheder i Linux

## Information
Formålet med denne øvelse er at udbygge din viden om brugerrettigheder i Linux og give dig færdighederne til at administrere og ændre disse rettigheder i praksis. Det er en vigtig del af systemadministration, da korrekt håndtering af rettigheder sikrer både funktionalitet og sikkerhed for F.eks at understøtte _Principle of least privilege_

Brugerrettigheder i Linux deles op i tre segmenter: ejeren af filens rettigheder, gruppen som er tilknyttet filens rettigheder, og til sidst alle andres rettigheder til filen.

Som udgangspunkt er der tre rettigheder, som kan tildeles en fil:

- **Read (r)** – Brugeren kan læse filen (og kopiere den).
- **Write (w)** – Brugeren kan skrive og ændre i filen.
- **Execute (x)** – Brugeren kan eksekvere filen som et program.

Hvis man ønsker at se rettighederne på en fil, kan dette gøres med kommandoen `ls -l`.

![file rettigheder](../../../Images/ØvelsesBilleder/Syssec/Øvelse%2010/fileRights.jpg)  
I det ovenstående eksempel har ejeren af filen rettigheder til at læse, skrive og eksekvere filen. Ingen andre end ejeren har rettigheder til denne fil.

Ligeledes kan rettighederne for et directory ses med kommandoen `ls -ld <Directory navn>`.  
![Directory rettigheder](../../../Images/ØvelsesBilleder/Syssec/Øvelse%2010/directoryRights.jpg)  
Bogstavet "d", som står først, indikerer, at rettighederne gælder for et directory. Ejeren har læse-, skrive- og eksekveringsretter. Eksekveringsrettigheden på et directory betyder, at man, selvom man ikke har læserettigheder, stadig kan tilgå indholdet (men ikke liste det med f.eks. `ls` kommandoen).

Kommandoen `chmod` anvendes til at tildele rettigheder til en fil. Man kan sætte rettighederne med enten tal eller bogstaver.

Hvis man bruger tal, er rækkefølgen for rettighedstildeling: `|Ejer|Gruppe|Alle andre|`.  
Nedenstående tabel viser, hvilken værdi der bruges til rettighedskombinationer:

| Værdi | Rettighed | Sum  |
|-------|-----------|------|
| 0     | ---       | 0+0+0|
| 1     | --x       | 0+0+1|
| 2     | -w-       | 0+2+0|
| 3     | -wx       | 0+2+1|
| 4     | r--       | 4+0+0|
| 5     | r-x       | 4+0+1|
| 6     | rw-       | 4+2+0|
| 7     | rwx       | 4+2+1|

For eksempel, hvis man vil give brugeren alle rettigheder og ingen rettigheder til andre, vil kombinationen være 700. Hvis man vil give ejeren læse- og skrivetilladelser, gruppen læsetilladelser, og eksekveringstilladelser til alle andre, er kombinationen 641.

Mere intuitivt kan man bruge bogstaver. Her vælger man hvilket segment der skal tildeles en rettighed med et bogstav:

| Bruger | Gruppe   | Andre |
|--------|----------|-------|
| u      | g        | o     |

Herefter bruger man +/- operatoren til at tildele rettighederne i forhold til en bestemt karakter:

| Read | Write | Execute |
|------|-------|---------|
| r    | w     | x       |

Eksempelvis vil kommandoen `chmod go-rwx` fratage gruppen og alle andre alle deres rettigheder.
  
Der kan findes uddybende beskrivelser i forberedelsen til idag, samt under _Yderlige resourcer_

## Links til beskrivelse af kommandoerne i opgaven:
- [chmod](https://linux.die.net/man/1/chmod)
- [chown](https://linux.die.net/man/1/chown)

## Instruktioner
I de følgende øvelser skal der arbejdes med at tildele og fjerne rettigheder fra filer og directories.  
**Udfør alle opgaver ved at tildele med både tal og bogstaver.**  
**Husk at fortsætte med at notere i dit Linux cheat sheet.**
**Du kan med fordel blot benytte din egen bruger, og ikke den du lavet i forrige øvelsels**

### Giv og fjern læserettigheder til en fil
I denne opgave skal der oprettes en fil og gives læserettigheder til alle andre.  
Fjern derefter rettigheden igen.

### Giv og fjern skrivetilladelser til en fil
I denne opgave skal der oprettes en fil og gives skrivetilladelser til gruppen.  
Fjern derefter rettigheden igen.

### Giv og fjern læserettigheder til et directory
I denne opgave skal der oprettes et directory og gives læserettigheder til alle andre.  
Fjern derefter rettigheden igen.

### Giv og fjern skrivetilladelser til et directory
I denne opgave skal der oprettes et directory og gives skrivetilladelser til gruppen.  
Fjern derefter rettigheden igen.

### Giv og fjern eksekveringsrettigheder til en fil
I denne opgave skal der oprettes en fil og gives eksekveringsrettigheder til gruppen.  
Fjern derefter rettigheden igen.

### Ændre ejeren af en fil
I denne opgave skal ejerskabet af en fil ændres til en anden bruger ved hjælp af kommandoen `chown`.

### Sårbarhed – For mange rettigheder
Reflekter over konsekvenserne ved for mange rettigheder. Hvorfor sker det nogle gange?  
Og hvorfor søger ondsindede brugere ikke nødvendigvis at få flere rettigheder?

## Links
- [chmod](https://linux.die.net/man/1/chmod)
- [chown](https://linux.die.net/man/1/chown)
