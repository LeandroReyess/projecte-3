# Tasca 01 - Gestors de Contrasenyes a EverPia 3

## Descripció de la tasca

**Alerta!!** EverPia ha estat atacada per ciberdelinqüents. La consultora on esteu de becaris ha patit una fuita d’informació (data breach) i informació confidencial sobre un projecte en desenvolupament està ara en mans de delinqüents que amenacen amb publicar-la si no es paga un rescat.

Aquest incident ha generat una gran alarma dins la companyia i s’ha creat un comitè de crisi per gestionar la situació. La investigació interna ha revelat que un dels comptes tècnics va ser compromès a causa de l'ús d'una contrasenya feble o reutilitzada.

### Objectiu

Com a resposta, la Direcció Tècnica ha emès la directriu que tot el personal tècnic ha de començar a utilitzar un **gestor de contrasenyes** validat, per garantir l'ús de credencials úniques i robustes.

Se us encarrega, doncs, la tasca d’analitzar diferents opcions de gestors de contrasenyes i elaborar la documentació necessària per a la formació del personal tècnic.

---

## Fase 1: Anàlisi i Justificació (Informe tècnic)

Heu de redactar un informe que inclogui:

- **Introducció i justificació:**  
  Explicació dels riscos associats a contrasenyes febles o reutilitzades (atacs de diccionari, credential stuffing, etc.) i la importància d’un gestor de contrasenyes per mitigar-los.

- **Comparativa tècnica:**  
  Taula detallada que compari almenys dues opcions:  
  - **Bitwarden (online / núvol):** sincronització, xifratge end-to-end, accés multi dispositiu, model freemium.  
  - **KeePassX / KeePassXC (offline / escriptori):** emmagatzematge local (fitxer KDBX), independència del núvol, open source, portabilitat.  

- **Avantatges i inconvenients:**  
  Resum dels pros i contres de cada model, considerant seguretat, usabilitat i continuïtat del negoci.

- **Recomanació:**  
  Elecció justificada de l’eina més adequada per a l’equip tècnic.

---

## Fase 2: Guia d’Ús Tècnica (Manual operatiu)

A partir de l’eina seleccionada a la fase 1, heu de crear una guia clara, amb captures de pantalla i instruccions pas a pas que cobreixi:

- **Instal·lació i configuració inicial:**  
  Descàrrega, instal·lació i creació de la base de dades o compte mestre.

- **Generació de contrasenyes segures:**  
  Ús del generador de contrasenyes amb paràmetres recomanats (longitud, caràcters especials, etc.).

- **Exemples pràctics d’ús i emplenament automàtic:**  
  - Com desar una credencial d’un compte de correu.  
  - Com desar una credencial d’una aplicació o servei web.  
  - Ús de l’extensió del navegador per a l’emplenament automàtic.  

- **Gestió de còpies de seguretat (backup):**  
  Procediments per fer còpies de seguretat segures (fitxer KDBX o exportació Bitwarden) i recomanacions per emmagatzemar-les (USB xifrat, núvol segur).

---

## Lliurament

- Crear la carpeta `tasca01` dins el repositori del projecte 3.  
- Dins `tasca01`, incloure:  
  - `README.md` (aquest fitxer amb la descripció i enllaços).  
  - `informe.md` amb el document de la Fase 1.  
  - `guia.md` amb la guia d’ús de la Fase 2.  
  - Carpeta `img/` (o similar) amb totes les imatges que s’incloguin a la guia.

---

## Materials i enllaços de suport

- [INCIBE: Gestió de contrasenyes segures](https://www.incibe.es/protege-tu-empresa/blog/gestion-contrasenas-seguras)  
- [Pàgina oficial de Bitwarden](https://bitwarden.com)  
- [Pàgina oficial de KeePassXC](https://keepassxc.org)  
- [INCIBE: Gestores de contraseñas: qué son y cómo pueden mejorar la seguridad de las empresas](https://www.incibe.es/protege-tu-empresa/blog/gestores-contrasenas-que-son-como-pueden-mejorar-seguridad-empresas)

---

## Notes finals

Aquesta tasca és individual i és fonamental per garantir la seguretat de la infraestructura i la confidencialitat dels projectes d’EverPia. La vostra feina ajudarà a protegir l’empresa davant futures amenaces.

---

*Benvinguts a EverPia 3. Poseu-vos la capa de superherois IT, que comença la defensa!*

