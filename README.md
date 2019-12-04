# EJS

## Qu'est-ce que EJS

Il s'agit d'un template qui génère du code HTML avec du javascript, il permet de rendre le code plus lisible avec une syntaxe simple. De plus, il permet par exemple avec un formulaire de récupérer de la data.

En résumer EJS c’est:
<ul>
    <li>Utiliser du javascript</li> 
    <li>Temps de développement rapide</li>
    <li>Syntaxe simple</li>
    <li>Exécution rapide</li>
    <li>Débogage facile</li>
    <li>Développement actif</li>
</ul>

Sa particularité est qu’il utilise des balises assez simple, par exemple:
<%=  			%>
Chevron ouvrant		Chevron fermant

Ces balises sont intégrées dans du code HTML comme ceci : <% = title %>  


## Comment utiliser ?
C'est un template qui fonctionne avec Node.js, il suffit de faire :
 
$ npm install ejs

## Sources:
Doc EJS:https://ejs.co/

Tuto_balises::https://medium.com/@Linda_Ikechukwu/https-medium-com-linda-ikechukwu-using-ejs-as-a-template-engine-in-your-express-app-cb3d82c15e17

Tuto_installation:https://openclassrooms.com/fr/courses/1056721-des-applications-ultra-rapides-avec-node-js/1057503-le-framework-express-js

# Socket.io

## Qu'est-ce que Socket.io
Il permet d’avoir une communication en temps réel , tout ce qui nécessite une communication immédiate entre les visiteurs de votre site peut en bénéficier. Il n’y a pas besoin de recharger la page

# Comment utiliser ?
Elle permet un échange bilatéral synchrone entre le client et le serveur contraire de Asynchrone.

# Comment utiliser ?
$ npm npm install socket.io<br>

Dans App.js ou fichier serveur<br>

var http = require('http').Server(app);<br>
var io = require('socket.io')(http);<br>

io.on('connection', () =>{
  console.log("client connecter")
 })<br>

Dans fichier HTML<br>
Balise script dans le head 
 src="/socket.io/socket.io.js">


## Sources:

 https://socket.io/docs/<br>
https://openclassrooms.com/fr/courses/1056721-des-applications-ultra-rapides-avec-node-js/1057825-socket-io-passez-au-temps-reel<br>
https://openclassrooms.com/fr/courses/1056721-des-applications-ultra-rapides-avec-node-js/1057959-tp-le-super-chat<br>


