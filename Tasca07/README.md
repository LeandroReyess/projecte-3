# 🧭 Implantació d’un Sistema de DNS Intern amb BIND9

## 📘 Descripció del projecte
Després de l’exitosa experiència a nivell de formació, els clients de **Digicore** estan tan satisfets amb la nostra feina que ens encarreguen la **implantació des de zero dels seus serveis de DNS interns**.

Actualment, l'agència utilitza **adreces IP** per accedir als servidors de desenvolupament, bases de dades i eines de gestió interna. Aquest mètode és **ineficient i propens a errors**:

- 🔢 **Usabilitat deficient:** Els empleats han de memoritzar o buscar constantment adreces IP complexes (p. ex. `192.168.10.25`).
- 🔧 **Manteniment feixuc:** Si un servidor canvia la seva IP, cal actualitzar manualment la configuració a tots els equips i aplicacions.
- 🧑‍💼 **Manca de professionalitat:** En un entorn professional, els serveis s’haurien d’accedir amb noms fàcils de recordar.

Per tant, la nostra missió és **implementar un Sistema de Noms de Domini (DNS) intern robust** que permeti accedir als servidors i aplicacions mitjançant **noms de domini amigables**, com per exemple:

# 🧭 Implantació d’un Sistema de DNS Intern amb BIND9

## 📘 Descripció del projecte
Després de l’exitosa experiència a nivell de formació, els clients de **Digicore** estan tan satisfets amb la nostra feina que ens encarreguen la **implantació des de zero dels seus serveis de DNS interns**.

Actualment, l'agència utilitza **adreces IP** per accedir als servidors de desenvolupament, bases de dades i eines de gestió interna. Aquest mètode és **ineficient i propens a errors**:

- 🔢 **Usabilitat deficient:** Els empleats han de memoritzar o buscar constantment adreces IP complexes (p. ex. `192.168.10.25`).
- 🔧 **Manteniment feixuc:** Si un servidor canvia la seva IP, cal actualitzar manualment la configuració a tots els equips i aplicacions.
- 🧑‍💼 **Manca de professionalitat:** En un entorn professional, els serveis s’haurien d’accedir amb noms fàcils de recordar.

Per tant, la nostra missió és **implementar un Sistema de Noms de Domini (DNS) intern robust** que permeti accedir als servidors i aplicacions mitjançant **noms de domini amigables**, com per exemple:

sudo apt install bind9 bind9utils bind9-doc -y

sudo named-checkconf
sudo named-checkzone digicore-XX.test /etc/bind/db.digicore-XX.test

sudo systemctl restart bind9
sudo systemctl enable bind9

dig @localhost bbdd.digicore-XX.test
dig -x 192.168.X.X

sudo apt install openssh-server -y
