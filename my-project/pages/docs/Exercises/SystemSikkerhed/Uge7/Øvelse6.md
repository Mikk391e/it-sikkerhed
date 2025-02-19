# Opgave 6 - Søgning i Linux file strukturen

1. I `Home directory`, eksekver kommandoen `find`.
    
    Finder alle filerne på systemet 
    
2. I `Home directory`, eksekver kommandoen `find /etc/`.
    
    Finder alle filerne i etc folderen
    
3. Eksekver kommandoen `sudo find /etc/ -name passwd`. *Sudo foran kommandoen betyder, at kommandoen eksekveres med de rettigheder, som sudo-gruppen har.*
    
    Finder filer med navnet passwd i den givne folder
    
4. Eksekver kommandoen `sudo find /etc/ -name pasSwd`. **Husk stort S**.
    
    Der findes ingen filer med navnet, da det er case sensitive
    
5. Eksekver kommandoen `sudo find /etc/ -iname pasSwd`. **Husk stort S**.
    
    Finder filer med navnet passwd i den givne folder. -iname gør at det er case insensitive
    
6. Eksekver kommandoen `sudo find /etc/ -name pass*`.
    
    Finder alle file med prefixet pass
    
7. `Home directory`, eksekver kommandoen `truncate -s 6M filelargerthanfivemegabyte`.
    
    Opretter en fil med en størrelse på 6 MB
    
8. I `Home directory`, eksekver kommandoen `truncate -s 4M filelessthanfivemegabyte`.
    
    Opretter en fil med en størrelse på 4 MB
    
9. I roden (/), eksekver kommandoen `find /home -size +5M`.
    
    Den finder alle filerne med en størrelse på over 5 MB
    
10. I roden (/), eksekver kommandoen `find /home -size -5M`.
    
    Den finder alle filerne med en størrelse på under 5 MB
    
11. I `Home directory`, opret to directories, et der hedder `test` og et andet som hedder `test2`.
12. I `test2`, skal der oprettes en fil som hedder `test`.
13. I `Home directory`, eksekver kommandoen `find -type f -name test`.
    
    Viser foldere med filer med navnet “test” i dem.
    
14. I `Home directory`, eksekver kommandoen `find -type d -name test`.
    
    Viser navnet på foldere med filer ved navn “test” i sig.