# **Fase 1 – Informe Tècnic: Administradors de Contrasenyes**

## **1. Introducció i Context**

L’incident de ciberseguretat sofert recentment per **EverPia** ha evidenciat una de les problemàtiques més comunes dins les empreses: la utilització de **contrasenyes insegures o repetides** en diferents serveis. Aquest fet facilita diversos vectors d’atac, entre els quals destaquen:

**Atacs de força bruta i diccionari:** Els atacants proven combinacions habituals i paraules comunes fins a encertar la contrasenya.  
**Credential stuffing:** Es reutilitzen credencials filtrades d’altres plataformes per intentar accedir als sistemes corporatius.  
**Phishing i enginyeria social:** Els usuaris poden acabar revelant les seves credencials a través de tècniques de manipulació o pàgines falses.  

Aquesta situació posa de manifest la importància d’utilitzar **contrasenyes robustes, diferents per a cada servei i protegides adequadament**.  

Els **gestors de contrasenyes** permeten solucionar aquesta problemàtica gràcies a funcionalitats com:

- Creació automàtica de contrasenyes segures i complexes.  
- Emmagatzematge xifrat de les credencials.  
- Accés controlat i sincronització entre diversos dispositius.  
- Reducció dels errors humans relacionats amb la reutilització de contrasenyes.  

Per aquest motiu, la Direcció Tècnica ha establert l’ús obligatori d’un gestor de contrasenyes aprovat per a tot el departament tècnic.

---

## **2. Comparació Tècnica**

| Característica | **Bitwarden** (Núvol / Online) | **KeePassXC** (Local / Offline) |
|----------------|--------------------------------|--------------------------------|
| **Sistema d’emmagatzematge** | Núvol de Bitwarden o servidor propi | Fitxer local en format KDBX |
| **Mètodes de xifratge** | AES-256 i PBKDF2-SHA256 amb xifratge end-to-end | AES-256 i ChaCha20 amb xifratge local |
| **Programari de codi obert** | Sí | Sí |
| **Compatibilitat multi-dispositiu** | Sí, amb apps i accés web | Sí, però mitjançant còpia manual del fitxer |
| **Sincronització automàtica** | Disponible al núvol | No disponible de forma nativa |
| **Generació de contrasenyes** | Inclosa i configurable | Inclosa i configurable |
| **Integració amb navegadors** | Extensions oficials per als principals navegadors | Integració mitjançant plugins |
| **Cost** | Model freemium | Totalment gratuït |
| **Sistema de còpies de seguretat** | Exportacions xifrades i backups automatitzats | Còpia manual del fitxer |
| **Portabilitat** | Molt elevada | Elevada |
| **Dependència d’Internet** | Sí (excepte autohospedatge) | No |
| **Facilitat d’ús** | Alta | Mitjana |

---

## **3. Punts Forts i Limitacions**

### **Bitwarden (Online / Núvol)**

**Avantatges:**
- Sincronització automàtica entre dispositius.  
- Interfície intuïtiva i moderna.  
- Accés des de navegador web, aplicació mòbil i escriptori.  
- Compatibilitat amb autenticació multifactor (2FA).  
- Possibilitat d’autohospedatge en empreses.

**Inconvenients:**
- Dependència d’una infraestructura en línia.  
- Possibles riscos associats al proveïdor, encara que el xifratge sigui end-to-end.  
- Algunes funcionalitats avançades requereixen subscripció.

---

### **KeePassXC (Offline / Local)**

**Avantatges:**
- Control complet sobre les dades i els fitxers.  
- No necessita connexió a Internet ni serveis externs.  
- Programari gratuït i de codi obert.  
- Fitxer portable i fàcil de transportar.

**Inconvenients:**
- La sincronització entre dispositius és manual.  
- Interfície menys amigable per a usuaris poc tècnics.  
- No incorpora backups automàtics de manera nativa.

---

## **4. Conclusions i Recomanació**

Després d’analitzar les dues alternatives, es considera que **Bitwarden** és la millor opció per implantar com a gestor corporatiu dins d’**EverPia**, principalment pels motius següents:

1. **Bon equilibri entre seguretat i comoditat d’ús**, gràcies al xifratge end-to-end i una interfície accessible.  
2. **Sincronització automàtica i accés des de múltiples dispositius**, molt útil per a equips tècnics.  
3. **Possibilitat de gestió centralitzada**, aplicació de polítiques de seguretat i control d’usuaris.  
4. **Projecte open source auditat**, fet que aporta transparència i confiança.  

Tot i això, en sistemes aïllats o entorns crítics sense connexió, **KeePassXC** continua sent una alternativa molt robusta per mantenir les credencials de manera local.  

Per tant, la proposta principal és implementar **Bitwarden**, preferiblement en versió Enterprise o mitjançant autohospedatge corporatiu.
