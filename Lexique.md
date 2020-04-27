# Lexique

# Similitudes et Différences entre MySQL et MongoDB ?

Ce sont tous les deux des bases de données open source. De plus MySQL a des similitudes avec mongodb qui sont:

<ul>
<li>Le principe tables(MySQL) et collections(MongoDb) son identique.</li>
<li>Dans une base de données MySQL, les informations sont stockées dans des tables ou collections.</li>
<li>Les lignes(MySQL) correspondent à un document(MongoDb)</li>
</ul>



Cependant, il existe des différence majeur comme par exemple que MySQL repose sur le principe du relationnel entre les tables, c'est-à-dire qu'on a la possibilité de faire des jointure, tandis que mongodb repose sur le principe du Nosql, c'est-à-dire pas de relation entre les documents.<br>

De plus pour communiquer avec la bdd de mysql il faut utiliser le langages SQL, ce qui n'est pas le cas de mongo qui lui ne possède pas de langage défini, les données dans les collections son stocké au format JSON ce qui permet de manipuler la bdd plus facilement<br>


Alors qui choisir ?

Tout dépend de ce que votre projet à besoin. S'il n'y a pas besoin de manipuler des relation entre les tables, on peut choisir mongo sinon mysql

# Qu’es qu'une MCD ?
MCD signifie modèle conceptuel de données, comme son nom l'indique, il s'agit d'un modèle qui permet de visualiser et structuré sa base de donnée avant de la crée.Les données sont représentées sous forme d'entités et d'associations entre entité.


# Definition ORM
Un mapping objet-relationnel est un programme(ORM) permet de simuler une base de donnée orientée objet à partir d’une base de données relationnelle.<br>
Il permet de crée des CRUD (création, lecture, mise à jour, suppression) et ainsi manipulé les donnée d'un base relationnel comme Mysql<br>

Exemple ORM:
<ul>
<li>- Sequelize: Supporte PostrgreSQL, MYSQL, MariaDB, SQLite and MSSQL</li>
<li>- Node-orm2: Supporte PostrgreSQL, MYSQL, Amazon Redshift and SQLite</li>
<li>- Objection.js: supporté par SQLite3, Postgres et MySQL.</li>
</ul>

# Langage objet et application hybride
La programmation orientée objet est un modèle de langage de programmation qui s'articule autour d'objets et de données. Les langages de programmations orientée objet sont :Java, Python, C++, Visual Basic .NET et Ruby <br>

Les applications hybrides sont des applications dites « cross-platform », il s’agit de déployer une seule version d’une application pour que celle-ci soit disponible sur toutes les plateformes.
# Qu'est-ce que l'Angular CLI ?
Command Line Interface (ou Interface en ligne de commande en français).Une interface en ligne de commande est une interface qui permet la communication entre un utilisateur et un ordinateur.

# Qu'es qui défini une API REST
Un api signifie Application Programming Interface.Les sites web et les applications ont besoin communiquer et échanger des données entre elle.
Les api REST signifie “Representational State Transfer”, il est basé sur la méthode http. Les critères d'un api rest sont:
<ul>
<li>Sans état: le serveur ne garde pas les infos du client req ->res</li>
<li>Cacheable (avec cache = mémoire): le client peut garder l'info </li>
<li>Orienté client-serveur: cominication client serveur</li>
<li>Avec une interface uniforme</li>
<li>Avec un système de couche</li>

</ul>























## Sources:
https://www.ionos.fr/digitalguide/web-marketing/vendre-sur-internet/les-meilleures-alternatives-a-paypal/
https://ecommerce-platforms.com/fr/articles/paypal-alternatives
Process d'achat sur paypal:https://www.primfx.com/integrer-paypal-express-checkout-son-site-php-496/payer-via-paypal-comment-marche/
https://www.economie.gouv.fr/dgccrf/Publications/Vie-pratique/Fiches-pratiques/Conditions-generales-de-vente
https://www.service-public.fr/professionnels-entreprises/vosdroits/F23455

