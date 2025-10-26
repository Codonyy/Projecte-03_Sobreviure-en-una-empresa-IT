
# Informe Tècnic: Implementació d’un Gestor de Contrasenyes a EverPia

## Fase 1:

## 1. Introducció i Justificació

### Risc de les contrasenyes febles o reutilitzades

L’ús de contrasenyes febles o repetides és una de les principals causes de ciberincidents empresarials. Aquestes pràctiques permeten diversos tipus d’atacs:

- **Atac de diccionari:** els atacants proven paraules i combinacions comunes fins a trobar una contrasenya vàlida.  
- **Força bruta:** s’assaiguen totes les combinacions possibles; les contrasenyes curtes o simples cauen en segons.  
- **Credential stuffing:** si una contrasenya filtrada s’utilitza en altres serveis, els atacants poden accedir-hi fàcilment.  
- **Phishing o enginyeria social:** la reutilització o l’apuntat de contrasenyes facilita que siguin robades.

Un sol compte compromès pot donar accés a dades sensibles o sistemes crítics.  
Per això, és essencial utilitzar **contrasenyes úniques, complexes i gestionades de manera segura** amb un **gestor de contrasenyes corporatiu**.

### La funció crucial d’un gestor de contrasenyes per mitigar aquests riscos

Un gestor de contrasenyes és una eina essencial per reduir els riscos derivats de l’ús de contrasenyes febles o reutilitzades.  
La seva funció principal és **emmagatzemar, generar i protegir credencials** de manera segura mitjançant xifratge avançat.

Les seves principals aportacions en seguretat són:

- **Generació automàtica de contrasenyes robustes:** permet crear contrasenyes úniques, llargues i complexes, difícils de trencar per força bruta o atacs de diccionari.  
- **Emmagatzematge segur i xifrat:** totes les credencials s’emmagatzemen en una base de dades protegida amb xifratge fort (AES-256), només accessible amb una contrasenya mestra.  
- **Evita la reutilització de contrasenyes:** el gestor facilita

## 2. Comparativa Tècnica


| Aspecte | Bitwarden | KeePassX / KeePassXC |
| ----- | ----- | ----- |
| **Model de seguretat** | Emmagatzema versions xifrades de les teves contrasenyes que només tu pots desbloquejar. | Emmagatzemar credencials en una base de dades local xifrada amb algorismes d'alta seguretat com AES-256. |
| **Accés multi-dispositiu** | Si | No |
| **Open Source** | No | Si |
| **Cost / Model Freemium** | de 4 a 6 euros | És gratuït |
| **Privadesa i control** | Depèn parcialment dels servidors Bitwarden (excepte en mode self-hosted). | Control i privadesa totals: les dades només resideixen al dispositiu de l’usuari. |
| **Còpies de seguretat** | Exportació i còpia automàtica al núvol o a un fitxer local xifrat. | Còpia manual del fitxer .kdbx a dispositius o suports segurs (p. ex. clau USB xifrada). |

<img src="/tasca1/img/Bitwarden.png" alt="Bitwarden logo" width="25%" height="25%"> <img src="/tasca1/img/keepassxc.jpg" alt="keepassxc logo" width="32%" height="32%">

## 3. Avantatges i inconvenients

**Bitwarden**  
Avantatges:
- Sincronització automàtica entre dispositius.
- Accessible des de navegador i mòbil.
- Administració centralitzada.  
Inconvenients:
- Dependència del núvol (possible vector d’atac).
- Requereix connexió a Internet.

**KeePassXC**  
Avantatges:
- Control total de les dades (fitxer local).
- Sense dependència del núvol.  
Inconvenients:
- Sincronització manual.
- Interfície menys intuïtiva per a usuaris no tècnics.

## 4. Recomanació

Des del meu punt de vista, recomano **Bitwarden** com a solució principal, per les seguents raóns:
- la seva **facilitat d’ús i sincronització** entre dispositius (ordinador, mòbil, navegador).
- el seu **model open source i xifratge end-to-end**.
- la **possibilitat de desplegar un servidor privat Bitwarden**, garantint control intern i seguretat.

# Fase 2: Guia d'Ús Tècnica (Manual Operatiu)

![solucio](/tasca1/img/cap1.png) 
![solucio](/tasca1/img/cap2.png) 
![solucio](/tasca1/img/cap3.png) 
![solucio](/tasca1/img/cap4.png) 
![solucio](/tasca1/img/cap5.png) 
![solucio](/tasca1/img/cap6.png) 
![solucio](/tasca1/img/cap7.png) 
![solucio](/tasca1/img/cap8.png) 
![solucio](/tasca1/img/cap9.png) 
![solucio](/tasca1/img/cap10.png) 
![solucio](/tasca1/img/cap11.png) 

1. Instal·lació i Configuració Inicial

Accedeix a https://bitwarden.com

Crea un compte nou amb una contrasenya mestra segura.

Inicia sessió i activa la verificació en dos passos (2FA).

2. Generació de Contrasenyes Segures

Fes clic a “Generador de contrasenyes”.

Configura longitud (mínim 16 caràcters).

Activa l’ús de majúscules, números i símbols.

Desa la nova contrasenya directament al gestor.

3. Exemples d’Ús i Emplenament Automàtic

Compte de correu:
Desa usuari i contrasenya del correu corporatiu.

Aplicació o servei web:
Desa credencials de GitHub, portals interns, etc.

Autocompletat:
Activa l’extensió de navegador → apareixerà l’opció d’emplenar automàticament.

4. Còpies de Seguretat

Des del client d’escriptori: Configuració → Export vault → .json xifrat.

Desa’l en una clau USB xifrada o servei de núvol segur (Google Drive xifrat o similars).

No comparteixis mai l’arxiu exportat sense xifrar.
