# 🌐 T06: Fonaments del servei DNS

## 📘 Descripció general

Com a membres de l’equip tècnic d’**EverPia**, aquesta tasca us situa davant un nou repte per al client **DigiCore**, una empresa de màrqueting digital que pateix problemes intermitents de connectivitat.  
El seu equip tècnic sospita que aquests errors podrien estar relacionats amb una **resolució de noms (DNS) incorrecta o lenta**.

L’objectiu de la tasca és **realitzar una auditoria teòrica i pràctica del servei DNS**, formant el personal del client i oferint eines de diagnosi ràpides i efectives per detectar i resoldre problemes de resolució de noms.

---

## 🎯 Objectius

1. Comprendre la **jerarquia i estructura del sistema DNS**.  
2. Explicar el **procés de resolució de noms** i els diferents tipus de consultes.  
3. Identificar i descriure els **tipus de zones i registres DNS més importants**.  
4. Entendre conceptes essencials com **SOA, TTL, Respostes Autoritatives i Reenviadors**.  
5. Conèixer la **resolució local i el protocol mDNS**.  
6. Posar en pràctica les eines de diagnosi DNS principals: **dig** i **nslookup**.  
7. Documentar i analitzar els resultats obtinguts durant la fase pràctica.  
8. Elaborar una **píndola formativa en vídeo** per al personal tècnic del client.

---

## 🧩 Estructura de la tasca

La tasca es divideix en dues fases principals:

---

## 🧠 **Fase Teòrica – Sessió formativa**

### 📚 Objectiu
Preparar material formatiu per al personal tècnic de DigiCore amb una explicació clara i visual dels fonaments del DNS.

### 📖 Continguts teòrics a desenvolupar

1. **Jerarquia i estructura del DNS**  
   - Root, TLDs, dominis de segon nivell.  
   - Estructura en arbre i delegació de responsabilitats.

2. **Procés de resolució de noms**  
   - Consultes iteratives i recursives.  
   - Servidors d’arrel i servidors autoritatius.

3. **Tipus de zones**  
   - Zona directa i zona inversa.  
   - Zona primària i secundària.

4. **Tipus de registres DNS (Records)**  
   - A, AAAA, CNAME, MX, NS, SRV.

5. **Conceptes essencials**  
   - **Resposta autoritativa:** com identificar-la i la seva importància.  
   - **TTL (Time To Live):** impacte en la propagació i rendiment.  
   - **SOA (Start of Authority):** contingut, número de sèrie, contacte administratiu.  
   - **Reenviadors:** condicionals i incondicionals.  
   - **Resolució local i mDNS (Multicast DNS).**

### 🎥 Activitat formativa
- Elaborar una **píndola formativa en vídeo (10-15 minuts)** que expliqui aquests conceptes de manera clara, visual i didàctica.  
- El vídeo ha d’incloure esquemes, exemples i breus demostracions pràctiques.

---

## 🧪 **Fase Pràctica – Diagnosi de noms (Auditoria CLI)**

### 🖥️ Objectiu
Aplicar eines de diagnosi DNS per avaluar la resolució de noms en diferents sistemes operatius (Linux/macOS i Windows), recollint i analitzant els resultats.

### ⚙️ Entorn de proves
- Equip virtual amb **Zorin OS** configurat amb **dues interfícies de xarxa**:  
  - NAT  
  - Adaptador pont amb IP configurada segons indicacions.  

---

### 🔍 A. Diagnosi avançada amb `dig` (Linux / macOS)

#### 🧩 Comandes i anàlisi

1️⃣ **Consulta bàsica de registre A**  
```bash
dig xtec.cat A

