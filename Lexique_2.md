# Lexique

# Notion JWT ?
Json Web Tokens est un format de token. Il permet de crée et générer un token d'indentification.
La struture de token se divise en 3 partie séparer de '.' 
<ul>
<li>Une en-tête: algo de chiffrement et type du token</li>
<li>
Les données: payload qui ont des donnée avec des champs (ex:nom user)</li>
<li>
La signature: valide ou  non du token</li>
</ul>
 Installation : npm i jsonwebtoken


# Introduction à l'accessibilité du web
De nos jour rendre les outils web accessible est important, un site ou  application peut être "bien coder" mais pas accéssible pour les personnes handicapée ou âgées.<br>
Rendre le web accessible est un avantage pour les internautes, les entreprises et la société.<br>

Qu’est-ce qui definesse l'accessibilité web ?


L’accessibilité du web comprend tous les handicaps affectant l’accès au web, en particulier le handicap :
<ul>
<li>auditif</li>
<li>cognitif</li>
<li>neurologique</li>
<li>physique de la parole</li>
<li>visuel</li>
</ul>
>
L’accessibilité du web bénéficie également aux personnes sans handicap, comme par exemple :
<ul>
<li>les personnes utilisant un téléphone mobile, une montre connectée, une télévision connectée, et autres périphériques ayant des petits écrans, différents modes de saisie, etc.</li>
<li>les personnes âgées dont les capacités changent avec l’âge</li>
<li>les personnes ayant un « handicap temporaire » tel qu’un bras cassé ou perdu leurs lunettes</li>
<li>les personnes ayant « une limitation situationnelle » comme être en plein soleil ou dans un environnement où elles ne peuvent pas écouter l’audio</li>
<li>les personnes utilisant une connexion internet lente ou ayant une bande passante limitée ou onéreuse</li>
</ul>

# Qu'est ce que le W3C ? A quoi sert il pour la création de site internet

Le W3C, World Wide Web Consortium, est un organisme international qui développe des standards pour le Web afin que les gens puissent communiquer efficacement à travers Internet.<br>

Les membres délèguent des ingénieurs au sein de W3C et participent ainsi à l'élaboration des spécifications techniques pour les technologies du Web comme par exemple rendre accessiblesles technos (html,css,xml,svg ect...)Le but de W3C de rendre accessible les soucres d'informations.

# L'intérêt d'un test unitaire

Un test unitaire permet de tester le bon fonctionnement d'une partie précise d'un programme. Il permet de s'assurer que le comportement d'une application est correct.<br>

L'avantage d'un test unitaire sont :<br>
<ul>

<li> permet d'avoir un retour rapide. Si le test échoue, vous pouvez corriger votre code 
</li>
<li>permet d'avoir un filet de sécurité. 
</li>
<li>permet d'éviter d'accumuler de la dette technique, en ayant une application qui soit facilement maintenable et évolutive.
</li>


</ul>

Pourquoi Mocha ?<br>
Il permet d'ecrire des test unitaire. L'idéal c'est d'ecrire les test avant de coder.Mocha n'est pas le seul Framework qui permet de créer des tests en JavaScript.<br>
Installation :npm install -g mocha

# Notion WebPack

En JavaScript pour inclure les libraires, il faut charger les fichiers dans les balises script dans notre page html. <br>
Le problématique étant qu'il devient de plus en plus lourd quand on charge plusieurs libraires avant notre fonction JavaScript.<br>
En node ce problème est résolue avec les inclusions grâce au module.export.<br>
WebPack permet de faire cela, ainsi, on évite d'inclure des libraire directement dans notre page html<br>

Installation :npm install --save-dev webpack@latest webpack-dev-server@latest

# Les Promise de node.js
L'objet Promise (pour « promesse ») est utilisé pour réaliser des traitements de façon asynchrone. Une promesse représente une valeur qui peut être disponible maintenant, dans le futur voire jamais.





















# sources
https://jwt.io/<br>
https://www.w3.org/WAI/fundamentals/accessibility-intro/fr<br>
http://communication-expert-comptable.over-blog.com/pages/Quest_ce_que_le_W3C_A_quoi_sert_il_pour_la_creation_de_site_internet-1950567.html<br>
https://openclassrooms.com/fr/courses/4568526-developpez-des-applications-robustes-et-fiables/4814730-decouvrez-l-importance-des-tests-unitaires<br>
https://www.grafikart.fr/tutoriels/premiers-tests-651<br>
https://www.alsacreations.com/tuto/lire/1754-debuter-avec-webpack.html




















