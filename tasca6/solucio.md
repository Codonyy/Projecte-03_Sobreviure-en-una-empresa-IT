
### Comanda 1: Consulta Bàsica de Registre A
**Consulta:** `dig xtec.cat A`

![solucio](/tasca6/img/cap1.png) 

**Anàlisi:**  
La resposta mostra la **adreça IP associada al domini xtec.cat**, que és el destí final al qual apunta el nom.  
El **valor TTL** indica el temps que aquesta resposta pot mantenir-se en memòria cau abans que calgui tornar a consultar-la.  
També s’identifica el **servidor que ha respost** a la consulta, que sol ser el servidor DNS configurat al sistema o el que s’indica explícitament en la comanda.

---

### Comanda 2: Consulta de Servidors de Noms (NS)
**Consulta:** `dig tecnocampus.cat NS`

![solucio](/tasca6/img/cap2.png) 

**Anàlisi:**  
Els resultats mostren els **servidors de noms autoritatius** responsables del domini tecnocampus.cat.  
Aquests servidors contenen la informació oficial del domini i són els que proporcionen respostes autoritzades a les consultes DNS relacionades amb ell.

---

### Comanda 3: Consulta Detallada SOA
**Consulta:** `dig escolapia.cat SOA`

![solucio](/tasca6/img/cap3.png) 

**Anàlisi:**  
A la resposta es pot veure el **registre SOA (Start of Authority)**, que inclou:
- El **servidor principal** del domini.  
- L’**adreça de correu de l’administrador** (en format adaptat DNS, substituint el “@” per un punt).  
- El **número de sèrie** de la zona, que indica la versió actual dels registres DNS i s’utilitza per sincronitzar còpies secundàries.

---

### Comanda 4: Consulta de Resolució Inversa
**Consulta:** `dig -x 147.83.2.135`

![solucio](/tasca6/img/cap4.png) 

**Anàlisi:**  
Aquest tipus de consulta permet saber **quin nom de domini està associat a una adreça IP**.  
El resultat mostra el **registre PTR**, que és l’equivalent invers del registre A.  
Això s’utilitza, per exemple, en processos de verificació o per identificar servidors dins de xarxes corporatives.

---

## B. Comprovació de Resolució amb `nslookup` (Multiplataforma)

L’eina **nslookup** és disponible tant a Linux (com Zorin OS) com a altres sistemes operatius.  
Permet realitzar consultes DNS interactives i comparar respostes obtingudes de diferents servidors.

---

### Comanda 1: Consulta Bàsica no Autoritativa
**Acció:**  
S’estableix `set type=A` i es consulta el domini `tecnocampus.cat`.

![solucio](/tasca6/img/cap5.png) 

**Anàlisi:**  
La resposta indica que és **no autoritativa** perquè prové d’un **servidor de memòria cau (cache)** i no del servidor autoritatiu del domini.  
Això significa que la informació és vàlida però ha estat obtinguda anteriorment d’una font autoritativa i guardada temporalment per millorar el rendiment.

---

### Comanda 2: Consultes Autoritatives
**Acció:**  
S’utilitza la comanda `server IP` per dirigir la consulta directament al **primer servidor de noms autoritatiu** obtingut en la consulta anterior.  
Després es torna a fer una consulta `set type=A` per al domini `tecnocampus.cat`.

![solucio](/tasca6/img/cap6.png) 
![solucio](/tasca6/img/cap7.png) 
![solucio](/tasca6/img/cap8.png) 

**Anàlisi:**  
La resposta ara és **autoritativa**, ja que prové directament del servidor que gestiona el domini.  
A diferència de la consulta anterior, aquesta resposta conté dades oficials i actuals del domini, sense passar per la memòria cau d’un altre servidor.  
També pot mostrar informació addicional del registre SOA o dels temps de propagació (TTL) reals.
