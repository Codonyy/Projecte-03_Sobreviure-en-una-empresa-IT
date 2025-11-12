# 🧩 Projecte: Implantació d’un Servei d’Autenticació Centralitzada amb OpenLDAP  
## Empresa: **Innovatech**

---

## 🏢 Context

**Innovatech**, una start-up tecnològica emergent, està experimentant un ràpid creixement. No obstant això, l’empresa pateix **problemes greus en la gestió dels seus usuaris i accessos**.  

Actualment:
Cada servei intern (servidor de fitxers, wiki de documentació, etc.) manté la seva **pròpia base de dades d’usuaris i contrasenyes**.
Els ordinadors clients utilitzen **autenticació local**, sense centralització.

Aquesta situació genera diversos problemes crítics:

---

## 🚀 Objectiu del Projecte

El **CEO d’Innovatech** ha contactat amb **EverPia** per desenvolupar una solució d’**autenticació centralitzada**.  
La proposta escollida és implantar **OpenLDAP (Lightweight Directory Access Protocol)** com a base per a la gestió d’usuaris i accessos.

### 🧱 Objectius específics

Implementar **OpenLDAP** en un servidor GNU/Linux.  
Configurar el **domini base** i la **jerarquia d’unitats organitzatives (OU)**.  
Crear i gestionar **usuaris i grups** dins del directori.  
Configurar **un equip client** perquè utilitzi el directori per **autenticar usuaris**.  
Assegurar que la infraestructura sigui **robusta, escalable i segura**, seguint els principis de programari lliure d’Innovatech.

---

## 🖥️ Tasques a Desenvolupar

1. **Instal·lació del servei OpenLDAP** al servidor Linux.  
2. **Configuració del domini base** segons l’estructura corporativa d’Innovatech.  
3. **Creació de la jerarquia LDAP:**
   - ou=usuaris
   - ou=grups
   - ou=departaments, etc.  
4. **Inserció d’usuaris i grups** dins del directori.  
5. **Configuració del client Ubuntu Desktop** per utilitzar el directori LDAP per a l’autenticació.  
6. **Verificació i proves de func**

## 📂 Índex de continguts

1. [📁 img/](./img/)
2. [📄 2. Requeriments d'Infraestructura Inicial.md](./2.%20Requeriments%20d'Infraestructura%20Inicial.md)
3. [📄 3. Tasques d'Implementació i Configuració del Servidor LDAP.md](./3.%20Tasques%20d'Implementació%20i%20Configuració%20del%20Servidor%20LDAP.md)
4. [📄 4. Integració de Client (Client Ubuntu Desktop).md](./4.%20Integració%20de%20Client%20(Client%20Ubuntu%20Desktop).md)
5. [📄 Acceptació del Plec de Condicions Tècniques (PCC) - EverPia.md](./Acceptació%20del%20Plec%20de%20Condicions%20Tècniques%20(PCC)%20-%20EverPia.md)
6. [📄 README.md](./README.md)
