# Øvelse 23 - Vulnerable Pentesting Lab Environment

### Information

Vulnerable Pentesting Lab Environment (VPLE) er en samling af web applikationer der med vilje er lavet med en masse usikkerheder indbygget. 
Miljøet er konfigureret i en virtuel maskine til vmware og kommer fra [vulnhub](https://www.vulnhub.com), der udover denne maskine tilbyder mange andre sårbare maskiner du kan afprøve.  

[VPLE](https://www.vulnhub.com/entry/vulnerable-pentesting-lab-environment-1,737/) indeholder disse web applikationer:

- [Web-dvwa](https://github.com/digininja/DVWA)   
- [Mutillidae](https://github.com/webpwnized/mutillidae)   
- [Webgoat](https://github.com/WebGoat/WebGoat)   
- [Bwapp](https://github.com/ajpalok/bWAPP)   
- [Juice-shop](https://github.com/juice-shop/juice-shop)   
- [Security-ninjas](https://github.com/opendns/Security_Ninjas_AppSec_Training)   
- Wordpress (source unknown....)  

Målet er at kunne dykke ned i kali værktøjerne og udforske dem på egne hånd, nu har du jo dit eget lille lab til at gøre det :-)  
Øvelsen her har mange timer i sig og jeg forventer ikke at du når den på en enkelt uge.  
Brug labbet når du læser om et specifikt kali værktøj og gerne vil øve det, eller hvis du vil afprøve en specifik sårbarhed.  

Nogle af kali værktøjerne du kan udforske er:  

- NMAP
- Burpsuite
- gobuster 
- dirbuster
- sqlmap
- john
- ffuf
- wfuzz
- wpscan

Find selv flere i [kali linux tool dokumentationen](https://www.kali.org/tools/)

Husk at bruge diagrammet når du arbejder.

![opnsense_intro_til_itsik2.png](../../../Images/ØvelsesBilleder/ITS/Uge10/Øvelse%2023/opnsense_intro_til_itsik2.png)  
*Netværksdiagram*

### Instruktioner

1. Hent VPLE VM [https://www.vulnhub.com/entry/vulnerable-pentesting-lab-environment-1,737/](https://www.vulnhub.com/entry/vulnerable-pentesting-lab-environment-1,737/)
3. Åbn maskinen i virtualbox [https://www.kali.org/docs/virtualization/import-premade-virtualbox/](https://www.kali.org/docs/virtualization/import-premade-virtualbox/)  
Hvis du ikke kan importere filen har Benny lavet en guide i E24 [Bennys guide til VPLE](https://bennyn86.gitlab.io/myportfolio/IT-Sikkerhed/Uge%2039%20-%20Netv%C3%A6rksanalyse/)  
Alternativt kan du hente den VPLE.ova fil jeg har lavet som også virker på virtualbox, den er på itslearning (men det er sejere at bruge Bennys guide!) 
4. Start VPLE maskinen i virtualbox.
4. Ret VPLE maskinens netværks konfiguration til det interne virtualbox netværk (intnet) som hører til OPT2 interfacet - se netværksdiagrammet hvis du er i tvivl.
5. VPLE maskinen henter en IP via DHCP hvilket ikke er konfigureret på opnsense routeren, derfor skal der konfigureres en statisk ip på VPLE maskinen.
6. Åbn en terminal til VPLE maskinen og find IP adressen med `hostname -I` - her finder du kun `172.17.0.1`. Der burder være 2 adresser, så der mangler en addresse til netværket.  
      - **TIP** *keyboard layoutet er sat til noget andet end dansk, du kan skrive `sudo loadkeys dk` for at skifte til dansk layout.*  
7. Find dit netværksinterfacenavn med `ip link | grep ens` (mit hedder ens33)
8. Åbn VPLE maskinens netværks konfiguration med  
`sudo nano /etc/netplan/01-netcfg.yaml`. 
9. Rediger filens indhold så det ser ud som nedenstående (ret ens33 hvis dit interface hedder noget andet):
   ```yaml
   network:
   version: 2
   renderer: networkd
   ethernets:
   ens33:
      dhcp4: no
      addresses:
         - 10.10.3.10/24
      gateway4: 10.10.3.1
   ```
10. Afslut nano med `ctrl+s` og derefter `ctrl+x`
11. Indlæs den nye configuration med `sudo netplan apply`
12. Kontroller at du har den korrekte ip addresse med `ip a | grep ens` og at du kan pinge routerens interface (OPT2, se netværks diagram for ip) *Fejlfind hvis det ikke virker*
13. Gå til din kali maskine, åbn en browser og naviger til VPLE maskinens ip, her burde du få en velkomst side der viser adresser til de forskellige labs *Fejlfind hvis det ikke virker*
14. Gå til DVWA og prøv et par øvelser fra [https://github.com/mrudnitsky/dvwa-guide-2019](https://github.com/mrudnitsky/dvwa-guide-2019) *Fejlfind hvis det ikke virker*
15. Udforsk de øvrige labs når du har tid og lyst fremover. Husk at dokumentere dine erfaringer på gitlab når du laver labs, det hjælper ved fejlfinding og fordrer dybdelæring.

## Links

- Kali linux tools dokumentation [https://www.kali.org/tools/](https://www.kali.org/tools/)
- Vulnhub [https://www.vulnhub.com](https://www.vulnhub.com)
- Ubuntu statisk ip artikel [https://linuxize.com/post/how-to-configure-static-ip-address-on-ubuntu-20-04/](https://linuxize.com/post/how-to-configure-static-ip-address-on-ubuntu-20-04/)
