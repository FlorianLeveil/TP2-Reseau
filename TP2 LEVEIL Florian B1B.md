# TP2 LEVEIL Florian B1B

## I. Exploration locale en solo

### 1.1 Affichage d'informations sur la pile TCP/IP locale

#### En CMD:

<img src="./TP2%20Screen/Ipconfigall%20-%2002.PNG">

**Nom, adresse MAC, adresse IP pour WIFI:**
* Carte réseau sans fil Wi-Fi
* 9C-B6-D0-09-AB-45
* 10.33.2.99

**Nom, adresse MAC, adresse IP pour Ethernet:**
* Carte Ethernet Ethernet
* 9C-B6-D0-09-AB-45
* J'en est pas

**Adresse de réseau:**
Calcule:
* 10.33.2.99 IP Base 10
* 0000.1010 0010.0001 0000.0010 0110.0011 IP
* 1111.1111 1111.1111 1111.1100 0000.0000 MASK
* 0000.1010 0010.0001 0000.0000 0000.0000 Adresse de Reseau
* 10.33.0.0 Adresse de Reaseau Base 10

**Adresse de broadcast:**
Calcule:
* 1111.1111 1111.1111 1111.1100 0000.0000 MASK
* 0000.1010 0010.0001 0000.0011 1111.1111 Brodcast
* 10.33.3.255 Brodcast Base 10

**Afficher la gateway:**
* 10.33.3.253 Parsserelle par défaut

#### En Graphique:

<img src="./TP2%20Screen/IPconfig%20Graph%20-03.PNG">


à quoi sert la gateway dans le réseau d'ingésup:
* Elle sert à relier un réseau Local (étudiant) au réseau mondial (Internet)

### 1.2 Modifications des informations

**A. Modification d'adresse IP**

<img src="./TP2%20Screen/ipconfig%20-%2004.PNG">

Calculez la première et la dernière IP du réseau:
* Première 10.33.0.0
* Dernière 10.33.3.256

**B. nmap**
<img src="./TP2%20Screen/Nmap%20-%2005.PNG">
<img src="./TP2%20Screen/Passerelle%20-%2007.PNG">
* Modifier l'IP: ça ne marche pas ! (Mais normalement soit doit marcher)
* Modifier la passerrelle: ça ne marche pas !

## II. Exploration Locale en duo
### Création d'un réseau / modification d'adresse IP

* Réseau /24:
<img src="./



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwMDEwMTcwNSwxOTk0NjE0MTQzLC02OT
Q3ODc3NTksMTMxMTEwNTg2MCwxMTM5NDQwNDU1LDE4NTA4MzI2
NSwtMTkzNjkyMzkzOV19
-->