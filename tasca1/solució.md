
# Informe Tècnic: Implementació d’un Gestor de Contrasenyes a EverPia

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

## 3. Comparativa Tècnica


| Aspecte | Bitwarden | KeePassX / KeePassXC |
| ----- | ----- | ----- |
| **Model de seguretat** | Emmagatzema versions xifrades de les teves contrasenyes que només tu pots desbloquejar. | Emmagatzemar credencials en una base de dades local xifrada amb algorismes d'alta seguretat com AES-256. |
| **Accés multi-dispositiu** | Si | No |
| **Open Source** | No | Si |
| **Cost / Model Freemium** | de 4 a 6 euros | És gratuït |
| **Privadesa i control** | Depèn parcialment dels servidors Bitwarden (excepte en mode self-hosted). | Control i privadesa totals: les dades només resideixen al dispositiu de l’usuari. |
| **Còpies de seguretat** | Exportació i còpia automàtica al núvol o a un fitxer local xifrat. | Còpia manual del fitxer .kdbx a dispositius o suports segurs (p. ex. clau USB xifrada). |

<img src="/tasca1/img/Bitwarden.png" alt="Bitwarden logo" width="25%" height="25%"> <img src="/tasca1/img/keepassxc.jpg" alt="keepassxc logo" width="32%" height="32%">



