# Sobre aquest programa...

## Què és LLXAMP?

LLxamp és una instància de Linux+Apache+PHP+MariaDB que pot ser utilitzada per a executar pràctiques estudiantils amb el llenguatge de programació PHP, aprendre a configurar un servidor web com Apache o bé aprendre a utilitzar sistemes de gestió de bases de dades MySQL/MariaDB.

## Per què necessite LLXAMP?

El programari contingut en Llxamp també pot ser obtingut des dels paquets del sistema operatiu, però en alguns casos pot presentar problemes si ja s'està utilitzant aquest programari per a altres tasques en el sistema i no es desitja utilitzar la instal·lació existent per a realitzar pràctiques que puguen deixar sense servei aquesta configuració.

A més, una instal·lació del sistema pot no ser suficient si es desitja que múltiples usuaris accedisquen a aquestes pràctiques en la mateixa màquina atés que la instal·lació en el sistema és única i requereix permisos d'administració per a la modificació dels fitxers de configuració.

## Característiques de LLXAMP

 - Permet instal·lar el programari perquè funcione en mode usuari tenint tota la instal·lació al directori d'usuari on poden ser modificats els fitxers per part de l'estudiant.
 - Permet l'ús de "hosts virtuals" (limitat a dominis .local) sense necessitat de permisos de superusuari.
 - És eficient en l'ús de disc, part de la instal·lació és compartida per tots els usuaris de la màquina.
 - Disposa d'una interfície gràfica per a l'arrancada/parada/estat dels servidors i modificació de fitxers importants, així com un visor per als registres que van generant.
 - Permet accessos amb SSL

## Com començar a utilitzar-lo?

Aquest programa encara que disposa de múltiples comandaments de línia d'ordres està pensat per a ser utilitzat des de la interfície gràfica *"llxamp-gui"* que pot ser llançada des de consola o bé des del menú d'aplicacions del sistema gràfic de l'entorn.

La primera vegada que és utilitzat per l'usuari encara no es disposa del programari instal·lat en la seua carpeta privada d'usuari *"$HOME"*, serà necessari preparar la instal·lació per a cada usuari des de l'únic botó actiu que presenta la interfície gràfica, posteriorment quan acabe el procés d'instal·lació ja és possible utilitzar tots els serveis i s'habilitaran totes les opcions en la interfície.

La instal·lació serà realitzada en la ruta *"$HOME/llxamp"* on l'usuari pot observar i modificar tots els fitxers de la instal·lació, no hi ha perill de trencar res del sistema atés que podria tornar a regenerar-se aquest directori forçant una altra reinstal·lació des de la interfície gràfica.

Si es desitgen modificar els fitxers de configuració, no és necessari utilitzar una altra eina diferent a la interfície gràfica Llxamp, des dels menús superiors poden editar-se els fitxers de configuració en ús pels serveis.

En la part dreta de la interfície es disposen botons que permeten realitzar les accions més habituals com són:

- Arrancar els serveis Apache i MariaDB.
- Parar els serveis actius.
- Obrir el navegador per a comprovar la pàgina que serveix Apache per defecte.
- Obrir el navegador per a comprovar la pàgina que serveix Apache utilitzant SSL.
- Obrir el navegador amb el portal d'administració PhpMyAdmin per a administrar del SGBD MariaDB.
- Mostrar els ports TCP utilitzats en el sistema.
- Mostrar els ports TCP disponibles en el sistema.
- Realitzar una còpia de seguretat de les dades que l'usuari ha modificat en la seua instal·lació des que va ser instal·lada.
- Mostrar un resum compacte de la configuració utilitzada en el servidor web Apache.
- Mostrar un resum compacte de la configuració utilitzada per PHP.

## Quina és la contrasenya inicial per a poder entrar a PhpMyAdmin?

La instal·lació inicial utilitza l'usuari "root" i contrasenya "root"

## Quina és la ruta per a accedir a PhpMyAdmin?

Per a poder accedir a PhpMyAdmin serà necessari utilitzar la ruta "/phpMyAdmin/index.php" exactament amb majúscules/minúscules a través del navegador.

## Quins ports utilitzen inicialment els serveis?

Inicialment els serveis són arrancats amb ports superiors > 1024, és una limitació a causa d'estar utilitzant aquests serveis com un usuari no privilegiat.

Quan són arrancats els serveis en la part baixa de la interfície poden observar-se els ports utilitzats així com el nombre de processos que cada servei té en ús.

Inicialment la instal·lació d'Apache utilitzarà els ports 8080 (no-SSL) i 8443 (SSL).

Inicialment la instal·lació de MariaDB utilitzarà el port 13306

## Com puc còmodament començar a servir pàgines web utilitzant la instal·lació PHP?

La carpeta per defecte per a deixar el contingut estàtic HTML o PHP és *"$HOME/llxamp/httpd/htdocs"*, allí es diposita inicialment:

- Un fitxer *index.html* (It works)
- Un fitxer *index.php* (Informació PHP)
- Un fitxer *db.php* (Indica les taules de la base de dades "test")

Si no es desitja utilitzar aquesta carpeta, també serà possible habilitar el mòdul *"user_dir"* del servei Apache (descomentant la línia corresponent en el fitxer de configuració Apache) i utilitzar la carpeta "public_html" del *"$HOME"* de l'usuari.

## Com puc utilitzar VirtualHosts?

Una limitació quan s'executa en mode usuari és que no poden modificar-se certs fitxers del sistema, per tant poden utilitzar-se sols dominis *.local*

Per a utilitzar-los s'han de configurar les corresponents seccions en el fitxer de configuració d'Apache utilitzant el domini desitjat,
Per exemple:

```
<VirtualHost exemple.local:8080>
    DocumentRoot "/webexemple"
    ServerName exemple.local

    # altres directives ací
</VirtualHost>
```

## Com puc utilitzar la instal·lació MariaDB des de línia de comandaments?

Es disposa d'una ordre *"llxamp-mysql"* que abreuja l'ús sense haver d'utilitzar paràmetres addicionals.
