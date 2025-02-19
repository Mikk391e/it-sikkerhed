# Opgave 8 - Processer og services i Linux

1. Eksekver kommandoen `ps`. *Resultatet skulle gerne ligne nedstående billede:*
    
    ![https://25f-its-syssec-a5e8ac.gitlab.io/exercises/Images/PSCommand.jpg](https://25f-its-syssec-a5e8ac.gitlab.io/exercises/Images/PSCommand.jpg)
    
    I venstre side af outputtet ses Process Id (PID). Hver process i Linux har et unikt ID. Herefter kommer *TeleTypewriter* (TTY), som viser hvilken terminal der eksekverede en kommando. CPU tid (TIME) viser det samlede CPU-tidsforbrug. Til sidst viser Command (CMD), hvilken kommando der eksekverede processen.
    
2. Eksekver kommandoen `ps -aux` *Denne gang vises processerne for alle brugere.*
    
    ![https://25f-its-syssec-a5e8ac.gitlab.io/exercises/Images/PSAUXCommand.jpg](https://25f-its-syssec-a5e8ac.gitlab.io/exercises/Images/PSAUXCommand.jpg)
    

Der er et par nye kolonner i outputtet; de mest interessante er %CPU, %MEM og STAT. %CPU og %MEM viser hver især det procentvise CPU- og hukommelsesforbrug. STAT viser processorens tilstand: S=Sleep but interruptible, R=Running, og T=Terminated.

1. Eksekver kommandoen `sudo apt install apache2 && sudo systemctl unmask apache2`.
2. Udskriv alle processer til konsollen og `grep` på ordet "apache2".

Bemærk tilstanden (STAT) er S. Altså, processen kører ikke, men venter på en hændelse. I de næste trin prøver vi at vække den.

1. Eksekver kommandoen `sudo apt install curl`. *Curl er et værktøj, som kan lave HTTP-forespørgsler til f.eks. Apache2 webserveren.*
2. Eksekver kommandoen `curl 127.0.0.1`. *Nu sendes der et HTTP-request til Apache2 webserveren.*
3. Gennemse outputtet og bekræft, at det er HTML fra Apache-serveren.