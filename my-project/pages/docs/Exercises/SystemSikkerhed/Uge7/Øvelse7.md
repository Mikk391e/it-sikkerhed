# Opgave 7 - Ændring og søgning i filer

1. I `Home directory`, eksekver kommandoen `touch minfile.txt`
    
    Laver en fil med navnet minfile
    
2. I `Home directory`, eksekver kommandoen `cp minfile.txt kopiafminfile.txt`
    
    laver en kopi af minfile med navnet kopiafminfile
    
3. I `Home directory`, eksekver kommandoen `mkdir minfiledir`
    
    Laver en folder med navnet minfiledir
    
4. I `Home directory`, eksekver kommandoen, `mv minfile.txt minfiledir`
    
    Rykker filen minfile.txt til minfiledir folderen
    
5. I `Home directory`, eksekver kommandoen, `rm -r minfiledir`
    
    Sletter folderen minfiledir, selv hvis folderen ikke er tom
    

1. I `Home directory`, eksekver kommandoen `echo "hej verden" > hejverdenfil.txt`
    
    Tager inputtet fra echo kommandoen og gemmer det i en fil
    
2. I `Home directory`, eksekver kommandoen `cat hejverdenfil.txt`
    
    Viser indholdet af hejverdenfilen
    
3. I `Home directory`, eksekver kommandoen `echo "hej ny verden" > hejverdenfil.txt`
    
    Erstatter indholdet af filen med det nye input
    
4. I `Home directory`, eksekver kommandoen `cat hejverdenfil.txt`
    
    Viser indholdet af hejverdenfilen
    
5. I `Home directory`, eksekver kommandoen `echo "hej endnu en ny verden" >> hejverdenfil.txt`
    
    Tilføjer inputtet til filen, uden at slette det oprindelige indhold
    
6. I `Home directory`, eksekver kommandoen `cat hejverdenfil.txt`
    
    Viser indholdet af hejverdenfilet
    

1. I `/etc/`, eksekver kommandoen `cat adduser.conf`.
    
    Viser indholdet af adduser.conf filen
    
2. I `/etc/`, eksekver kommandoen `cat adduser.conf | grep 1000`.
    
    Viser linjerne i filen, som indeholder 1000
    
3. I `/etc/`, eksekver kommandoen `cat adduser.conf | grep no`.
    
    Viser linjerne i filen, som indeholder “no”
    
4. I `/`, eksekver kommandoen `grep no /etc/adduser.conf`
    
    Gør det samme som forrige kommando
    
5. I `/`, eksekver kommandoen `ls -al | grep proc`
    
    Viser alle filer og foldere, som indeholder proc 
    
6. I `/etc/`, eksekver kommandoen `ls -al | grep shadow`
    
    Viser alle filer og foldere med shadow i sig