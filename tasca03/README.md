# 🧩 T03: Gestió flexible de discos (LVM i Espais d’emmagatzematge)

## 📘 Descripció general

En aquesta tasca posarem en pràctica els coneixements sobre **gestió flexible de l’emmagatzematge** mitjançant dues tecnologies clau:

- **LVM (Logical Volume Manager)** en entorns **Linux (Zorin OS o similar)**.  
- **Espais d’emmagatzematge (Storage Spaces)** en **Windows 11**.

L’objectiu és **dissenyar, implementar i documentar dues solucions d’emmagatzematge** per satisfer les necessitats del nostre client **Garriga i Associats**, un bufet d’advocats que gestiona grans quantitats d’informació legal sensible.  

Aquestes solucions han de garantir:
- **Alta disponibilitat**: continuïtat del servei davant fallades de disc.  
- **Redundància**: protecció de dades mitjançant miralls o paritat.  
- **Escalabilitat**: possibilitat d’ampliar l’espai sense interrupcions.  

El treball es farà en màquines virtuals, com a **prova de concepte (PoC)**, documentant tots els procediments i resultats obtinguts.

---

## 🧠 Objectius

1. Dissenyar i implementar una solució d’emmagatzematge flexible i redundant amb **LVM a Linux (Zorin OS)**.  
2. Dissenyar i implementar una solució equivalent amb **Espais d’emmagatzematge a Windows 11**.  
3. Documentar detalladament els passos realitzats, configuracions i proves de funcionament.  
4. Presentar una proposta tècnica per al client amb les conclusions i avantatges de cada tecnologia.

---

## 🐧 Part 1 – LVM a Linux (Zorin OS)

### 🔧 Requisits i procediments

- **Configuració inicial:**  
  Creació d’un *Volume Group (VG)* i un *Logical Volume (LV)* a partir de dos discos de 10 GB.  
  El volum s’ha de formatar i muntar automàticament mitjançant `/etc/fstab`.

- **Alta disponibilitat:**  
  Implementació d’un **mirall (lvm_mirror)** per garantir la integritat de les dades davant la fallada d’un disc.

- **Instantànies (Snapshots):**  
  1. Afegir dos nous discos de 10 GB al grup de volums.  
  2. Crear un volum nou `lvm_dades`, formatar-lo i muntar-lo.  
  3. Afegir fitxers (per exemple, imatges descarregades).  
  4. Crear un **snapshot (`lv_snapshot`)** i demostrar el procés de **restauració** en cas de corrupció de dades.

- **Escalabilitat:**  
  Demostrar l’ampliació del volum `lv_dades` aprofitant l’espai lliure del grup de volums.

### 📄 Documentació

➡️ [Documentació LVM (Linux)](./LVM_linux.md)

---

## 🪟 Part 2 – Espais d’emmagatzematge a Windows 11

### 🔧 Requisits i procediments

- **Configuració inicial:**  
  Creació d’un **Storage Pool** amb tres discos de 10 GB (simulats).

- **Estudi de configuracions:**  
  - **Mirroring:** Usar dos discos i comprovar la redundància davant fallades.  
  - **Paritat:** Usar tres discos i analitzar l’eficiència d’espai en comparació amb el mirall.  
  - **Mirall triple:** Afegir els discos necessaris per provar aquesta configuració.

- **Gestió i monitoratge:**  
  Mostrar com es pot consultar l’estat del pool, els discos i la salut del sistema des de la consola de gestió de Windows.

### 📄 Documentació

➡️ [Documentació Espais d’emmagatzematge (Windows)](./StorageSpaces_windows.md)

---

## 🤝 Organització del treball

El treball es realitzarà **en grup**, dividint les tasques en dos equips:

- **Equip Linux:** Configuració i documentació del sistema LVM.  
- **Equip Windows:** Configuració i documentació dels Espais d’emmagatzematge.

Cada membre:
1. Buscarà i provarà les comandes i configuracions necessàries.  
2. Documentarà el procés individualment.  
3. Revisarà conjuntament la documentació final.  
4. Pujarà la seva versió al repositori dins la carpeta `tasca03/`.

---

## 📂 Estructura del projecte


