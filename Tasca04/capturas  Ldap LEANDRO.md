Un cop dins, actualitzem els paquets:

sudo apt update && sudo apt upgrade \-y

Editem el fitxer /etc/hosts per definir el domini:

![image1](image1.png)

![image2](image2.png)
Verifiquem que els canvis s’han aplicat correctament al domini.

![image3](image3.png)

Per permetre la comunicació amb l’amfitrió, configurem una interfície Host-Only:  
![image4](image4.png)
![image5](image5.png)
Editarem l’arxiu /etc/netplan/50-cloud-init.yaml amb la comanda següent per habilitar la interfície:

![image6](image6.png)


Instal·lem el servidor LDAP i les utilitats:


![image7](image7.png)

Durant la instal·lació, el sistema ens demanarà la contrasenya de l’administrador. Introduirem p@ssw0rd, tal com s’indica al Plec de Condicions Tècniques.

![image8](image8.png)

![image9](image9.png)
![image10](image10.png)
!![image11](image11.png)

Un cop executada la comanda anterior, comprovarem que el servei s’està executant correctament amb la següent comanda:

![image12](image12.png)
Ara comprovarem que el directori s’ha creat amb el nom desitjat:  
![image13](image13.png)
Ara haurem de crear dues unitats organitzatives (*OUs*): users i groups, mitjançant un fitxer .ldif.

Per fer-ho, crearem l’arxiu OU\_users.ldif amb la següent comanda:

![image14](image14.png)
A dins del fitxer hi afegirem el contingut següent:

![image15](image15.png)

Per crear finalment les OUs, executarem la comanda següent:  
![image16](image16.png)
Ara els grups:  
![image17](image17.png)

![image18](image18.png)

Per crear finalment les OUs, executarem la comanda següent:  
![image19](image19.png)
Per comprovar que les OUs s’han afegit correctament, utilitzarem la comanda següent:

![image20](image20.png)
Com que administrar el servidor de domini des de la línia d’ordres pot resultar complex, és recomanable utilitzar un gestor d’usuaris LDAP com LDAP Account Manager (LAM).

Per instal·lar-lo, executarem la comanda següent (el paràmetre \-y evita que apareguin missatges de confirmació durant la instal·lació):

![image21](image21.png)

Un cop instal·lat, ens hi connectarem des de la màquina física a través de la interfície host-only, introduint la seva adreça IP seguida de /lam al navegador:

![image22](image22.png)
A continuació, apareixerà el panell d’inici de sessió, on la contrasenya per defecte és lam.  
![image23](image23.png)
En aquest apartat configurarem les opcions generals del gestor, com ara l’idioma, el compte d’administrador i altres paràmetres bàsics.

![image24](image24.png)
A la segona pestanya Account Types, definirem els DN dels usuaris i dels grups, incloent-hi una OU per als usuaris i una altra per als grups.

Tot seguit, apareixerà el panell d’inici de sessió, on accedirem amb l’usuari administrador del domini:

![image25](image25.png)

![image26](image26.png)
![image27](image27.png) 
**Un cop dins d’aquest apartat, farem clic a New group per crear els dos grups.**  


![image28](image28.png)


**epetirem el mateix procés per crear un usuari per a cada grup, anomenats tech01 i manager01.**

**Per fer-ho, ens dirigirem a Accounts → Users i farem clic a New user.**

 **l’interior del formulari haurem d’introduir la informació personal de l’usuari, com ara l’adreça, el telèfon, la fotografia i altres dades bàsiques.**

**En aquest pas, haurem de crear el grup primari amb el mateix nom que l’usuari.**  
**Haurem d’afegir l’usuari al grup corresponent.**

**Per fer-ho, farem clic al botó Edit groups i, un cop dins, mourem el grup tech (en aquest cas) a la secció Selected groups per assignar-lo correctament a l’usuari.**

![image29](image29.png)
![image30](image30.png)
![image31](image31.png)
![image32](image32.png)
![image33](image33.png)
![image34](image34.png)
![image34](image34.png)
![image35](image35.png)
![image35](image35.png)
![image36](image36.png)
**Un cop dins del client, haurem de configurar el nom de l’equip perquè formi part del mateix domini que el servidor.**

**Com que no disposem d’un servei DNS, editarem el fitxer /etc/hosts del client per tal que pugui resoldre el nom del servidor correctament.**
![image37](image37.png)
![image38](image38.png)


**Ara comprovarem que els noms es resolen correctament executant les comandes següents:**

**Per assegurar-nos que el nom de l’equip s’ha canviat correctament:**

![image39](image39.png)

**Per verificar que la resolució DNS cap al servidor de domini és correcta:**


![image40](image40.png)

### **Instal·lació dels mòduls d’autenticació LDAP**

**Per poder utilitzar el client dins del domini, hem d’instal·lar els mòduls necessaris amb la comanda següent:**
![image41](image41.png)

**A continuació, s’iniciarà el procés de configuració dels mòduls d’autenticació.**



![image42](image42.png) 
![image43](image43.png) 
![image44](image44.png)
![image45](image45.png)
![image46](image46.png)

![image47](image47.png)
![image48](image48.png)
![image49](image49.png)
**Per comprovar la connectivitat amb el servidor, farem una consulta ldapsearch des del client amb la comanda següent:**
![image50](image50.png)
![image51](image51.png)
Ara configurarem l’arxiu nsswitch.conf per indicar que s’utilitzarà LDAP per a la gestió d’usuaris i grups.
![image52](image52.png)

Al fitxer /etc/pam.d/common-password, eliminarem la línia que contingui el terme use\_authok.  

Al fitxer /etc/pam.d/common-session, afegirem la línia següent per permetre la creació automàtica dels perfils d’usuari:




Un cop el servei s’hagi reiniciat, comprovarem que detecta correctament els usuaris LDAP amb aquesta comanda:

![image52](image52.png)
![image53](image53.png)
![image54](image54.png)
![image55](image55.png)
![image56](image56.png)
![image57](image57.png)
![image58](image58.png)
Per finalitzar, editarem el fitxer /etc/pam.d/gdm-launch-environment per permetre l’inici de sessió gràfica dels usuaris del domini.  
![image59](image59.png)
Reiniciarem el client i, a la pantalla d’inici de sessió, farem clic a Not listed per introduir manualment un altre usuari.  
![image60](image60.png)
Un cop iniciada la sessió, podem comprovar que tot s’ha creat correctament.  
![image61](image61.png) 
Si repetim el mateix procés amb l’usuari manager01, obtindrem el mateix resultat.  


