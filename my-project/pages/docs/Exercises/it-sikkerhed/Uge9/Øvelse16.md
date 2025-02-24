# Øvelse 16 - Opsætning af virtuelle maskiner i VirtualBox

## Information

Til at lære netværk i faget bruges VirtualBox som hypervisor, opnsense som router/firewall og diverse linux distributioner som hosts på netværket. Opnsense opsættes i senere øvelser, i denne øvelse er det 2 hosts der skal installeres/konfigureres.

Den ene host skal bruge bruge seneste stable version af [lubuntu](https://lubuntu.me/downloads/) som image. Den host installeres som var det en fysisk maskine, det vil sige at der i VirtualBox oprettes en virtuel maskine, der vælges antal cpu, ram etc. og lubuntu .iso filen (imaget) indsættes i det virtuelle cdrom drev på maskinen.

Den anden maskine skal bruge bruge seneste kali [linux vm image](https://www.kali.org/get-kali/#kali-virtual-machines) til VirtualBox. Dette er allerede en VirtualBox maskine der blot skal åbnes og ikke behøver at blive installeret på samme måde som lubuntu imaget.

Formålet med øvelsen er at lære hvordan hosts konfigureres i VirtualBox på forskellige måder.

I denne og de følgende øvelser som omhandler netværk bruges nedenstående netværksdiagram til at konfigurere netværkets enheder efter.
Diagrammet er lavet i draw.io
draw.io filen kan i hente her: [opnsense_intro_til_itsik0.drawio](https://ucl-pba-its.gitlab.io/25f-its-intro/exercises/diagrams/opnsense_intro_til_itsik0.drawio)

![Netværksdiagram](../../../Images/ØvelsesBilleder/ITS/Uge9/Netværksdiagram.png)

## Instruktioner

1. Lav 1 lubuntu VM maskine i VirtualBox, brug seneste stable version af lubuntu som image.
hjælp til at installere en ny vm https://www.virtualbox.org/manual/UserManual.html#create-vm-wizard



2. Importer Kali Linux VirtualBox imaget fra https://www.kali.org/get-kali/#kali-virtual-machines
Hjælp til at importere et VM image i VirtualBox https://www.kali.org/docs/virtualization/import-premade-virtualbox/



3. Konfigurer de 2 virtuelle maskiner's netværk ifølge netværks diagrammet, det vil sige statisk ip konfigureres på begge maskiner med ip adresser fra diagrammet.
Hjælp til at konfigurere netværk på en VM i VirtualBox https://www.virtualbox.org/manual/UserManual.html#settings-network

    

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2016/image1.png)

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2016/image2.png)

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2016/image3.png)

![img](../../../Images/ØvelsesBilleder/ITS/Uge9/Øvelse%2016/image4.png)

## Links

* [lubuntu](https://lubuntu.me/downloads/)
* [kali vm images](https://www.kali.org/get-kali/#kali-virtual-machines)