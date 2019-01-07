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
<img src="./TP2%20Screen/Capture09.PNG">
<img src="./TP2%20Screen/Capture08.PNG">

* Réseau/20:

<img src="./TP2%20Screen/capture10.PNG">
<img src="./TP2%20Screen/capture11.PNG">

### Utilisation d'un des deux comme gateway

* Quand mon pc utilise la gateway pour avoir accès internet:
Ipconfig:
``` PS C:\Users\Florian> ipconfig

Configuration IP de Windows


Carte Ethernet Ethernet :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::70de:8f61:ddbb:d1fc%9
   Adresse IPv4. . . . . . . . . . . . . .: 192.168.137.20
   Masque de sous-réseau. . . . . . . . . : 255.255.255.0
   Passerelle par défaut. . . . . . . . . : 192.168.137.1

Carte réseau sans fil Connexion au réseau local* 3 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 11 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . : auvence.co

Carte Ethernet Connexion réseau Bluetooth :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :


```
Curl Google:
```PS C:\Users\Florian> curl google.com


StatusCode        : 200
StatusDescription : OK
Content           : <!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="fr"><head><meta
                    content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta
                    content="/images/branding/googleg/1x/goo...
RawContent        : HTTP/1.1 200 OK
                    X-XSS-Protection: 1; mode=block
                    X-Frame-Options: SAMEORIGIN
                    Cache-Control: private, max-age=0
                    Content-Type: text/html; charset=UTF-8
                    Date: Thu, 20 Dec 2018 10:16:41 GMT
                    Expires: ...
Forms             : {f}
Headers           : {[X-XSS-Protection, 1; mode=block], [X-Frame-Options, SAMEORIGIN], [Cache-Control, private,
                    max-age=0], [Content-Type, text/html; charset=UTF-8]...}
Images            : {@{innerHTML=; innerText=; outerHTML=<IMG id=hplogo onload=window.lol&amp;&amp;lol()
                    style="PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT: 0px" alt=Google
                    src="/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png" width=272
                    height=92>; outerText=; tagName=IMG; id=hplogo; onload=window.lol&amp;&amp;lol();
                    style=PADDING-BOTTOM: 14px; PADDING-TOP: 28px; PADDING-LEFT: 0px; PADDING-RIGHT: 0px; alt=Google;
                    src=/images/branding/googlelogo/1x/googlelogo_white_background_color_272x92dp.png; width=272;
                    height=92}}
InputFields       : {@{innerHTML=; innerText=; outerHTML=<INPUT type=hidden value=fr name=hl>; outerText=;
                    tagName=INPUT; type=hidden; value=fr; name=hl}, @{innerHTML=; innerText=; outerHTML=<INPUT
                    type=hidden value=hp name=source>; outerText=; tagName=INPUT; type=hidden; value=hp; name=source},
                    @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden name=biw>; outerText=; tagName=INPUT;
                    type=hidden; name=biw}, @{innerHTML=; innerText=; outerHTML=<INPUT type=hidden name=bih>;
                    outerText=; tagName=INPUT; type=hidden; name=bih}...}
Links             : {@{innerHTML=<SPAN class=gbtb2></SPAN><SPAN class=gbts>Recherche</SPAN>; innerText=Recherche;
                    outerHTML=<A onclick=gbar.logger.il(1,{t:1}); id=gb_1 class="gbzt gbz0l gbp1"
                    href="https://www.google.fr/webhp?tab=ww"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Recherche</SPAN></A>; outerText=Recherche; tagName=A; onclick=gbar.logger.il(1,{t:1});;
                    id=gb_1; class=gbzt gbz0l gbp1; href=https://www.google.fr/webhp?tab=ww}, @{innerHTML=<SPAN
                    class=gbtb2></SPAN><SPAN class=gbts>Images</SPAN>; innerText=Images; outerHTML=<A
                    onclick=gbar.logger.il(1,{t:2}); id=gb_2 class=gbzt
                    href="http://www.google.fr/imghp?hl=fr&amp;tab=wi"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Images</SPAN></A>; outerText=Images; tagName=A; onclick=gbar.logger.il(1,{t:2});;
                    id=gb_2; class=gbzt; href=http://www.google.fr/imghp?hl=fr&amp;tab=wi}, @{innerHTML=<SPAN
                    class=gbtb2></SPAN><SPAN class=gbts>Maps</SPAN>; innerText=Maps; outerHTML=<A
                    onclick=gbar.logger.il(1,{t:8}); id=gb_8 class=gbzt
                    href="http://maps.google.fr/maps?hl=fr&amp;tab=wl"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Maps</SPAN></A>; outerText=Maps; tagName=A; onclick=gbar.logger.il(1,{t:8});; id=gb_8;
                    class=gbzt; href=http://maps.google.fr/maps?hl=fr&amp;tab=wl}, @{innerHTML=<SPAN
                    class=gbtb2></SPAN><SPAN class=gbts>Play</SPAN>; innerText=Play; outerHTML=<A
                    onclick=gbar.logger.il(1,{t:78}); id=gb_78 class=gbzt
                    href="https://play.google.com/?hl=fr&amp;tab=w8"><SPAN class=gbtb2></SPAN><SPAN
                    class=gbts>Play</SPAN></A>; outerText=Play; tagName=A; onclick=gbar.logger.il(1,{t:78});;
                    id=gb_78; class=gbzt; href=https://play.google.com/?hl=fr&amp;tab=w8}...}
ParsedHtml        : mshtml.HTMLDocumentClass
RawContentLength  : 45839 
```
Quand mon collègue ce connecte à internet via mon pc:
* J'ai une version Insider de Windows je n'ai pas l'option "Ethernet"

<img src="./TP2%20Screen/capture12.PNG">

### Chat privé
Une fois sur le même réseau et avec le même port ça donne ça:
<img src="./TP2%20Screen/Capture13.PNG">

### Wirechark
Pendant un ping et un message:

<img src="./TP2%20Screen/capture14.PNG">

Voici les trames concernant les messages en question:

<img src="./TP2%20Screen/capture15.PNG">

Trier les trames avec "tcp.stream eq 0":

<img src="./TP2%20Screen/capture16.PNG">

### Firewall
Gestion des règles:

<img src="./TP2%20Screen/capture17.PNG">

Gestion IP:

<img src="./TP2%20Screen/capture18.PNG">

Gestion protocole:

<img src="./TP2%20Screen/capture19.PNG">

Nous avons essayé de nous Ping avec ceci mais ça ne marche pas !

## III. Manipulations d'autres outils/protocoles côté client
### 1. DHCP
 * Adresse IP du serveur DHCP du réseau WiFi:
 ```
  Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . : auvence.co
   Description. . . . . . . . . . . . . . : Killer Wireless-n/a/ac 1535 Wireless Network Adapter
   Adresse physique . . . . . . . . . . . : 9C-B6-D0-09-AB-45
   DHCP activé. . . . . . . . . . . . . . : Oui
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::5c55:b0b4:ada6:95d9%20(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.2.111(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.252.0
   Bail obtenu. . . . . . . . . . . . . . : lundi 7 janvier 2019 13:36:57
   Bail expirant. . . . . . . . . . . . . : lundi 7 janvier 2019 16:36:58
   Passerelle par défaut. . . . . . . . . : 10.33.3.253
   Serveur DHCP . . . . . . . . . . . . . : 10.33.3.254
   IAID DHCPv6 . . . . . . . . . . . : 329037520
   DUID de client DHCPv6. . . . . . . . : 00-01-00-01-22-FE-5E-05-D8-CB-8A-F3-F1-D5
   Serveurs DNS. . .  . . . . . . . . . . : 10.33.10.20
                                       10.33.10.7
                                       8.8.8.8
   NetBIOS sur Tcpip. . . . . . . . . . . : Activé 
   ```
   L’adresse du serveur DHCP est: ```10.33.3.254 ```
 *  Date d'expiration du bail DHCP: ```lundi 7 janvier 2019 16:36:58 ```
 *   Nouvelle adresse IP (en ligne de commande):
 1.  ipconfig /flushdns:
 ```
 PS C:\Users\Florian> ipconfig /release

Configuration IP de Windows

Aucune opération ne peut être effectuée sur Connexion au réseau local* 3 lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion au réseau local* 11 lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion réseau Bluetooth lorsque
son média est déconnecté.

Carte Ethernet Ethernet :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 3 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 11 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::5c55:b0b4:ada6:95d9%20
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet Connexion réseau Bluetooth :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :
 ```
2.  ipconfig /release:
```
PS C:\Users\Florian> ipconfig /release

Configuration IP de Windows

Aucune opération ne peut être effectuée sur Connexion au réseau local* 3 lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion au réseau local* 11 lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion réseau Bluetooth lorsque
son média est déconnecté.

Carte Ethernet Ethernet :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 3 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 11 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . :
   Adresse IPv6 de liaison locale. . . . .: fe80::5c55:b0b4:ada6:95d9%20
   Passerelle par défaut. . . . . . . . . :

Carte Ethernet Connexion réseau Bluetooth :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :
   ```
3.  ipconfig /renew:
```
PS C:\Users\Florian> ipconfig /renew

Configuration IP de Windows

Aucune opération ne peut être effectuée sur Ethernet lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion au réseau local* 3 lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion au réseau local* 11 lorsque
son média est déconnecté.
Aucune opération ne peut être effectuée sur Connexion réseau Bluetooth lorsque
son média est déconnecté.

Carte Ethernet Ethernet :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 3 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Connexion au réseau local* 11 :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :

Carte réseau sans fil Wi-Fi :

   Suffixe DNS propre à la connexion. . . : auvence.co
   Adresse IPv6 de liaison locale. . . . .: fe80::5c55:b0b4:ada6:95d9%20
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.2.111
   Masque de sous-réseau. . . . . . . . . : 255.255.252.0
   Passerelle par défaut. . . . . . . . . : 10.33.3.253

Carte Ethernet Connexion réseau Bluetooth :

   Statut du média. . . . . . . . . . . . : Média déconnecté
   Suffixe DNS propre à la connexion. . . :
   ```
### 2. DNS
#### IP du serveur DNS:
Faire un ipconfig /all
```
 Serveurs DNS. . .  . . . . . . . . . . : 10.33.10.20
                                       10.33.10.7
                                       8.8.8.8
```

#### nslookup:
```
> nslookup
Serveur :   UnKnown
Address:  10.33.10.20
```
#### lookup:
* Pour  `google.com`:
```
> lookup google.com
Serveur :   google.com
Addresses:  2a00:1450:4007:805::200e
          216.58.208.238
```
* Pour  `ynov.com`:
```
> lookup ynov.com
Serveur :   ynov.com
Address:  217.70.184.38

DNS request timed out.
    timeout was 2 seconds.
DNS request timed out.
    timeout was 2 seconds.
```
* Résultats de ces commandes:
ça affiche l'adresse du nom de domaine.
#### reverse lookup_ :
* pour l'adresse  `78.78.21.21`:
```
PS C:\Users\Florian> nslookup 78.78.21.21
Serveur :   UnKnown
Address:  10.33.10.20

Nom :    host-78-78-21-21.mobileonline.telia.com
Address:  78.78.21.21
```
* pour l'adresse  `92.16.54.88`
```
PS C:\Users\Florian> nslookup 92.16.54.88
Serveur :   UnKnown
Address:  10.33.10.20

Nom :    host-92-16-54-88.as13285.net
Address:  92.16.54.88
```

* Résultats:

ça affiche le nom du serveur, l'adresse, le nom de l'host et l'adresse de l'host.








<!--stackedit_data:
eyJoaXN0b3J5IjpbLTUxODgwNzI2MCwtMTk2ODczNDUyLC0xOT
kzODIyNjk3LDQ0OTI2MzcwMiwtOTk1NjE2ODQ1LC04ODQwNzU1
NTAsLTE4ODE3NjE0MTIsLTEyOTA5NTY5NDAsLTM0OTI0MjYzMS
wxMTcwMDA2ODQ4LC0xNzg3NjY5MzgxLDg3NTAyODE4NCwxMDI0
NTQyLDE5OTQ2MTQxNDMsLTY5NDc4Nzc1OSwxMzExMTA1ODYwLD
ExMzk0NDA0NTUsMTg1MDgzMjY1LC0xOTM2OTIzOTM5XX0=
-->