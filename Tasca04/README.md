# 🧩 T03: Implementació d’un servei d’autenticació centralitzada amb OpenLDAP

## 🏢 Context: Innovatech i la necessitat de centralització

**Innovatech**, una start-up tecnològica en ple creixement, està experimentant un caos en la gestió dels seus usuaris i accessos.  
Actualment, cada servei intern (servidor de fitxers, wiki de documentació, etc.) manté la seva **pròpia base de dades d’usuaris i contrasenyes**, i els **ordinadors clients** utilitzen **autenticació local**.  

Aquesta situació genera diversos **problemes crítics**:

- ⚙️ **Ineficiència operativa:** cada alta o baixa de personal obliga a crear o eliminar comptes en múltiples sistemes.
- 🔐 **Risc de seguretat:** la reutilització de contrasenyes entre serveis és freqüent.
- 📈 **Manca d’escalabilitat:** a mesura que creix el nombre de serveis, la gestió es torna insostenible.

---

## 🎯 Objectiu de la tasca

El **CEO d’Innovatech** ha contactat amb **EverPia** per implementar una **solució d’autenticació centralitzada** mitjançant **OpenLDAP (Lightweight Directory Access Protocol)**.  

Aquesta tecnologia permetrà:
- Centralitzar la gestió d’usuaris i grups.
- Simplificar l’autenticació i l’autorització d’accés.
- Millorar la seguretat i l’eficiència en l’administració dels sistemes.
- Facilitar la integració amb altres serveis de xarxa (servidors de fitxers, intranets, aplicacions internes...).

---

## 🧠 Aprenentatges i competències

Durant aquesta tasca, aprendràs a:

1. 🧰 **Instal·lar i configurar OpenLDAP** en un servidor GNU/Linux.  
2. 🧱 **Definir el domini base** i la **jerarquia d’unitats organitzatives (OU)** segons les necessitats d’Innovatech.  
3. 👥 **Crear i gestionar usuaris i grups** dins del directori.  
4. 💻 **Integrar un equip client** al directori LDAP per autenticar-se contra el servidor central.  
5. 🔍 **Verificar i provar** el funcionament de l’autenticació centralitzada.

---

## ⚙️ Desenvolupament del projecte

### 1. Instal·lació del servei OpenLDAP
- Instal·lació dels paquets necessaris (`slapd`, `ldap-utils`).
- Configuració inicial del servidor i definició del domini (ex. `dc=innovatech,dc=local`).

### 2. Configuració del domini i jerarquia
- Creació de les **Unitats Organitzatives (OU)**:  
  - `ou=usuaris`
  - `ou=grups`
  - `ou=departaments`
- Disseny del **fitxer LDIF** per afegir els elements bàsics al directori.

### 3. Creació d’usuaris i grups
- Afegir usuaris amb atributs LDAP estàndard (uid, cn, sn, mail...).
- Assignar-los a grups segons el departament o la funció.

### 4. Configuració del client LDAP
- Instal·lació i configuració dels paquets (`libnss-ldap`, `libpam-ldap`, `nslcd` o `sssd`).
- Modificació dels fitxers `/etc/nsswitch.conf` i `/etc/pam.d/common-*`.
- Proves d’autenticació (`getent passwd`, inici de sessió LDAP, etc.).

### 5. Verificació i proves
- Comprovar que els usuaris definits al directori poden autenticar-se des del client.  
- Validar la sincronització i la resposta del servei LDAP.

---

## 🧩 Plec de condicions tècniques

El document amb tots els **requeriments tècnics detallats** està disponible al **Moodle de l’assignatura**, dins del mòdul corresponent a **Serveis de Directori**.  
Allà trobaràs els passos exactes, comandes i configuracions que cal seguir per completar correctament la implementació.

---

## 📚 Material de classe (disponible al Moodle)

- **UD04.AA1:** Serveis de Directori  
- **UD04.AA2:** Instal·lació OpenLDAP  
- **UD04.AA3:** Configuració del Directori  
- **UD04.AA5:** Agregar Client al Directori  

---

## 🧾 Lliurament i avaluació

Un cop finalitzada la pràctica:
1. Presenta un **informe tècnic** documentant tot el procés (instal·lació, configuració, proves).  
2. Adjunta les **captures de pantalla** o sortides de terminal que demostrin el correcte funcionament.  
3. Respon el **qüestionari d’avaluació** disponible al Moodle per validar els coneixements adquirits.

---

## 💡 Conclusió

Amb aquesta pràctica, Innovatech passarà d’un sistema desorganitzat i insegur a una **infraestructura centralitzada, segura i escalable**.  
A més, consolidaràs coneixements essencials sobre **OpenLDAP**, **autenticació centralitzada** i **administració de sistemes Linux** dins del marc de **seguretat informàtica** d’EverPia.

---

> “Centralitzar l’autenticació no només millora la seguretat, sinó que allibera temps per innovar.” 🚀

