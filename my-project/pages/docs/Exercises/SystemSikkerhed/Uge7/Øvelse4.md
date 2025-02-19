# Opgave 4 - Linux file struktur

Linux Cheat sheet

1. Eksekver kommandoen `pwd`
    
    pwd - printer nuværende folder
    
2. Eksekver kommandoen `cd /`
    
    cd / - går til roden af filsystemet
    
3. Lokationen `/` har en bestemt betydning i Linux-filsystemet. Hvad er det? (Her kan du med fordel søge svar på Google).
    
    / - er roden af filsystemet
    
4. Eksekver kommandoen `cd /etc/ca-certificates/`. Hvad findes der i directoriet?
    
    cd /etc/ca-certificates/ - her finder man certifikater, som man har tillid til
    
5. Hvor mange *directories* viser outputtet fra `pwd` kommandoen når den eksekveres i directoriet fra forrige trin?
    
    Der vises 2 directories
    
6. Eksekver kommandoen `cd ../..`.
    
    Går op to foldere
    
7. Hvor mange *directories* viser outputtet fra `pwd` kommandoen nu?
    
    Den viser ikke nogen
    
8. Eksekver kommandoen `cd ~` (Karakteren hedder tilde. I Ubuntu kan den nogen gange findes med knappen F6).
    
    Dette går til brugerens hjemmefolder
    
9. Kommandoen `~` er en "genvej" i Linux, hvad er det en genvej til?
    
    Brugerens hjemmefolder
    
10. I filsystemets rod (`/`), eksekver kommandoen `ls`.
    
    Viser mapper og filer i den nuværende folder
    
11. I brugerens *home directory*, eksekver kommandoen `touch helloworld.txt`.
    
    Opretter en fil med filnavnet helloworld.txt
    
12. I brugerens *home directory*, eksekver kommandoen `nano helloworld.txt`.
    
    Åbner programmet nano som er en teksteditor
    
13. List alle filer og mapper i brugerens *home directory*.
    
    
14. List alle filer og mapper i brugerens *home directory* med flaget `a`.
    
    Lister alle filer, også gemte
    
15. List alle filer og mapper i brugerens *home directory* med flaget `l`.
    
    Viser informationer omkring filerne
    
16. List alle filer og mapper i brugerens *home directory* med flaget `la`.
    
    Viser alle filer og mapper, samt informationer heromkring
    
17. I brugerens *home directory*, eksekver kommandoen `mkdir helloWorld`.
    
    Laver en ny folder med navnet helloWorld
    
18. Eksekver kommandoen `ls -d`.
    
    
19. Eksekver kommandoenn `ls -f`.

### **Opgave 4 - Linux file struktur**

/ - Her ligge alle filer og mapper på systemet

|_bin - Essential binaries

|_boot - Her ligger filer som er nødvendige for, at systemet kan starte

 

|_dev - Det er Device filer, så det kan være hardware eksponeret som filer

|_etc - Konfigurationsfiler

|_home - Indeholder brugerspecifikke konfigurationer og andre brugerspecifikke filer

|_media - Her vises flytbare medieenheder, såsom en cd el.lign.

|_lib - Indeholder biblioteker, som filerne i bin skal bruge 

|_mnt - Her installere man midlertidige fil systemer. Dette kan f.eks. være i forbindelse med filgenoprettelse

|_misc - idk, et eller andet med understøttende filer, som ikke er essentielle

|_proc - Indeholder filer, som repræsenterer systemet og proces information

|_opt - Indeholder underfoldere for ikke essentielle software pakker. Så et program kan eventuelt smide sine filer ind i der her directory

|_sbin - Indeholder essentielle binære filer til system administration

|_root - Root home directory, hvilket er hjemmefolderen for root brugeren

|_tmp - Midlertidige filer, disse filer gemmes ikke mellem hver opstart af systemet

|_usr - Indeholder filer og applikationer som bruges af brugerne

|_var - Vigtigst af alt findes logfiler her