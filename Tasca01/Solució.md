# Informe: Gestors de Contrasenyes per a l’Equip Tècnic

**Projecte:** T01 - Fase 1: Anàlisi i Justificació (Document d'Informe)  
**Data:** 21 d’octubre de 2025  
**Autor:** Leandro Linares de los Reyes  

---

## 🗂️ Índex
1. [Per què fem aquest informe?](#1-per-què-fem-aquest-informe)
   - [Per què són perilloses les contrasenyes febles o reutilitzades?](#per-què-són-perilloses-les-contrasenyes-febles-o-reutilitzades)
   - [Com ens pot ajudar un gestor de contrasenyes?](#com-ens-pot-ajudar-un-gestor-de-contrasenyes)
2. [Comparació entre dos gestors: Bitwarden i KeePassXC](#2-comparació-entre-dos-gestors-bitwarden-i-keepassxc)
3. [Pros i contres de cada opció](#3-pros-i-contres-de-cada-opció)
   - [Bitwarden (Online - Núvol)](#bitwarden-online---núvol)
   - [KeePassXC (Offline - Local)](#keepassxc-offline---local)
4. [Què recomanem?](#4-què-recomanem)

---

## 1. Per què fem aquest informe?

Després del **ciberatac** que ha patit l’empresa, s’ha descobert que els atacants van entrar fent servir el compte d’un tècnic amb una contrasenya **feble o reutilitzada**.  
Això va permetre accedir a informació crítica del projecte, i ara els atacants demanen diners a canvi de no publicar-la.

A causa d’aquest incident, la direcció ha decidit que tots els tècnics han de començar a fer servir **un gestor de contrasenyes**.

---

### Per què són perilloses les contrasenyes febles o reutilitzades?

Els ciberdelinqüents utilitzen programes automàtics per atacar comptes de diverses maneres:

- 🔑 **Atac de diccionari:** proven contrasenyes típiques com `123456` o `password`.
- 🧩 **Credential stuffing:** proven contrasenyes robades d’altres serveis per veure si funcionen aquí.
- ⚙️ **Brute force:** proven milers de combinacions fins que troben la bona.

---

### Com ens pot ajudar un gestor de contrasenyes?

Un gestor de contrasenyes permet:

- 🔐 Crear **contrasenyes segures i diferents** per a cada web o servei.  
- 💾 **Guardar-les de manera segura**, evitant que les hagis de recordar.  
- ⚡ **Autocompletar-les** automàticament quan calgui.

Així es redueix molt el risc d’un nou atac causat per errors humans.

---

## 2. Comparació entre dos gestors: Bitwarden i KeePassXC

| Característica                | **Bitwarden (Online)**        | **KeePassXC (Offline)**     |
|-------------------------------|--------------------------------|------------------------------|
| **On es guarda?**             | Al núvol (internet)            | A l’ordinador o USB          |
| **Sincronització**            | Sí, entre tots els dispositius | No, s’ha de fer a mà         |
| **Accés des del mòbil o web** | Sí, molt fàcil                 | Més complicat                |
| **És codi obert?**            | Sí                             | Sí                           |
| **Preu**                      | Gratuït / Pagament opcional    | Gratuït                      |
| **Nivell de seguretat**       | Molt alt (xifrat end-to-end)   | Molt alt (tot queda local)   |
| **Fàcil d’utilitzar?**        | Sí, intuïtiu                   | Una mica més tècnic          |
| **Ideal per equips?**         | Sí, permet compartir dades     | No pensat per treball en equip |

---

## 3. Pros i contres de cada opció

### **Bitwarden (Online - Núvol)**

**Pros:**
- Fàcil d’instal·lar i fer servir.  
- Funciona en mòbils, web i ordinador.  
- Sincronització automàtica entre dispositius.  
- Ideal per treballar en equip.  
- Compatible amb **autenticació en dos factors (2FA)**.

**Contres:**
- Les dades es guarden al núvol (cal confiar en el servei).  
- Algunes funcions extra requereixen la versió de pagament.

---

### **KeePassXC (Offline - Local)**

**Pros:**
- Tot queda **en local**, control total de les dades.  
- No depèn d’internet per funcionar.  
- Completament **gratuït i de codi obert**.

**Contres:**
- Cal copiar l’arxiu manualment per usar-lo en altres dispositius.  
- Més complex per a usuaris no tècnics.  
- Poc pràctic per a treball en equip.

---

## 4. Què recomanem?

### ✅ **Recomanació: Bitwarden**

Després d’analitzar les dues opcions, **Bitwarden** és la millor opció per a l’equip tècnic de l’empresa.

**Motivacions:**
- Fàcil d’instal·lar i utilitzar, fins i tot per a no experts.  
- Compatible amb tots els dispositius (mòbil, web, PC).  
- Sincronització automàtica de contrasenyes.  
- Permet compartir accés de manera segura entre membres de l’equip.  
- És segur, de **codi obert**, i transparent en el seu funcionament.

**KeePassXC** també és una bona opció per a ús personal o entorns totalment locals, però **no és pràctic per equips col·laboratius** com el d’EverPia.

---

> **Fase 2:** A determinar en futures etapes del projecte.

---

