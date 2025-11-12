
# 🧩 T03: Gestió flexible de discos (LVM i Espais d’emmagatzematge)

## 📝 Breu descripció

Després de completar la fase de formació, l’equip tècnic d’**EverPia** ha rebut un nou encàrrec del bufet **Garriga i Associats**, un dels més prestigiosos de la ciutat. Aquesta empresa gestiona una gran quantitat d’informació legal sensible, fet que fa que la **integritat**, la **disponibilitat** i la **facilitat de gestió** del seu emmagatzematge siguin aspectes crítics.

El client necessita renovar els seus sistemes de servidors per:
- Garantir la protecció davant fallades de disc.
- Permetre l’ampliació d’espai sense interrupcions del servei.

Com a tècnics d’EverPia, l’objectiu és **dissenyar i documentar dues solucions d’emmagatzematge**:
1. Una per a entorns **Linux (LVM)**.
2. Una per a entorns **Windows (Storage Spaces)**.

Aquestes solucions hauran de complir amb els principis de **redundància**, **alta disponibilitat** i **escalabilitat**.  
La implementació es farà amb **màquines virtuals**, com a prova de concepte.

---

## 🐧 Part Linux: LVM amb Zorin OS

### Requisits d’implementació i demostració

#### ⚙️ Configuració inicial
- Crear un **grup de volums (VG)** i un **volum lògic (LV)** amb **dos discs de 10 GB**.
- Formatar i muntar automàticament el volum editant l’arxiu `/etc/fstab`.

#### 🔁 Alta disponibilitat
- Implementar un **mirall (lvm_mirror)** per protegir la informació davant fallades de disc.

#### 🧩 Instantànies (Snapshots)
- Afegir **dos discs addicionals de 10 GB** al grup de volums.
- Crear un volum `lvm_dades` amb el primer disc, formatar-lo i muntar-lo.
- Afegir arxius al volum (p. ex. imatges d’Internet).
- Crear un **snapshot (lv_snapshot)** amb el segon disc i documentar com restaurar-lo en cas de corrupció de dades.

#### 📈 Escalabilitat
- Mostrar el procés d’ampliació del volum `lv_dades` usant l’espai lliure del grup de volums.

---

## 🪟 Part Windows: Espais d’Emmagatzematge (Storage Spaces)

### Requisits d’implementació i demostració

#### ⚙️ Configuració inicial
- Crear un **Storage Pool** amb **tres discs de 10 GB**.

#### 🧠 Estudi de configuracions
- **Mirroring (Resiliència de mirall):** utilitzar dos discs i comprovar l’alta disponibilitat.  
- **Parity (Resiliència de paritat):** explicar la seva eficiència d’espai respecte al mirall. (Requereix tres discs.)  
- **Triple Mirroring:** afegir els discs necessaris per demostrar aquesta configuració.

#### 🖥️ Gestió i manteniment
- Mostrar l’estat dels discs i del pool des de la **consola de gestió de Windows**.
- Documentar la **facilitat de manteniment** i monitoratge del sistema.

---

## 🤝 Metodologia de treball

1. **Divisió en equips:**
   - Equip 1 → Gestió en **Linux (LVM)**  
   - Equip 2 → Gestió en **Windows (Storage Spaces)**

2. **Fases de treball:**
   - Preparar el **guió individual** amb comandes i documentació tècnica.
   - Fer la **implementació i demostració** per parelles.
   - Revisar conjuntament la documentació generada.
   - Cada membre ha de **pujar la documentació** al seu repositori.

3. **Estructura de la carpeta del projecte:**
