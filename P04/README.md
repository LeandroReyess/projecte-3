# 🖥️ P04: Documentació Servidor DNS

## 📘 Breu descripció
Molt benvinguts a la vostra nova tasca, consultors!  
Com a membres de l'equip de **sistemes d'EverPia**, heu configurat un servidor de noms com a **prova de concepte** pel client **Digicore**.  
Actualment, la vostra configuració es troba dins d’una **màquina virtual**, i l’objectiu d’aquesta tasca és **publicar els fitxers de configuració a GitHub**. D’aquesta manera, qualsevol replicació futura serà ràpida i segura: només caldrà descarregar els arxius al servidor Linux i reiniciar el servei per tenir el servidor completament operatiu.

---

## ⚙️ Fase 1: Preparació de la connectivitat i extracció dels arxius

### Pas 1.1: Configuració de la interfície Host-Only
1. A la configuració de la màquina virtual Ubuntu Server, afegiu una **segona interfície de xarxa** en mode **Host-Only**.  
2. Configureu i activeu la interfície.  
3. Comproveu que hi ha connectivitat amb la màquina física (host).

### Pas 1.2: Còpia segura dels fitxers amb SCP
Un cop establerta la connectivitat, utilitzeu **SCP (Secure Copy Protocol)** per transferir els fitxers de configuració a la màquina física:

**Arxius a copiar:**
- `/etc/bind/named.conf.options`  
- `/etc/bind/named.conf.local`  
- Arxius de zones dins de `/etc/bind/zones`

**Exemple de comanda SCP:**
```bash
scp usuari@IP_VM:/etc/bind/named.conf.options .
scp usuari@IP_VM:/etc/bind/named.conf.local .
scp usuari@IP_VM:/etc/bind/zones/* ./zones/


