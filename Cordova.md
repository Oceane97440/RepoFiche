# sommaire 

 - [installer cordova](#install-cordova)
 - [install android studio](#install-android-studio)
 - [install gradle](#install-gradle)
 - [install sdk](#install-sdk)
 - [variable d'environnement a rajouter ](#variable-denvironnement-a-rajouter)
 - [autorisé l'ajax dans votre application](#autorisé-lajax-dans-votre-application)
 - [Erreur rencontrer](#Erreur-rencontrer)
 - [ajax request GET POST PUT DELETE](#ajax-request-GET-POST-PUT-DELETE)
 - [ajouté un logo](#add-logo)


# install cordova 
```
$ npm install -g cordova
$ cordova create MyApp
$ cd MyApp 
$ cordova platform add browser
$ cordova run browser
```
### pour crer une platefrom : 

 ```$ cordova build android ``` <br>
 ```$ cordova build ios```  <br>
```$ cordova build browser ```

# <span>&#9888;</span> attention  <span>&#9888;</span>: 
si vous voulez compiler et que vous avez fait des modifications dans vos variables d'environnements ou changer de version java, sdk, jre, ect.... ou encore rajouter des plugins ou modifier le fichier config.xml 

### il faut :
``` 
$ cordova platform remove android //(suppression de l'ancienne plateform )
$ cordova platform add android //(ajout de la plateform avec les modifications que vous aurez apporté )
```
# install android studio 

ceci ne devrai pas etre trop compliquer <br><br>
Je vous conseille toutefois de telecharger la version ```"android 10.0 api 29"``` en plus de la version conseiller par l'IDE


# install gradle
- Telecharger gradle 6.7.1 
- creer un fichier  ```C:\Gradle ``` et décompresser ici 
- dans variable d'environnement ajouter a variable systeme Path  ```C:\Gradle\gradle-6.7.1\bin```
- verifier avec ```$ gradle -v ```(si info c'est bon)
- si c pas ok cree un variable environement "GRADLE_HOME" ```C:\Gradle\gradle-6.7.1\bin```


# install sdk 

https://www.oracle.com/fr/java/technologies/javase-jdk15-downloads.html

- creer une variable d'environnement utilisateur JAVA_HOME avec pour destination ```C:\Program Files\Java\jdk-15.0.1\```
- fermer le terminal de commande en ouvrir un autre et faire la commande ``` javac --version ``` (si resultat ok)


# variable d'environnement a rajouter 

vous pouvez verifier les requirements avec ```cordova requirements android --verbose``` <br><br>
### <span>&#9888;</span> pour chaque modification vous devez reouvrir votre terminal pour que les modifications soient effectives
<br>

### (remplacer ```${user}``` par votre nom )
<br>

ANDROID_HOME
```C:\Users\${user}\AppData\Local\Android\Sdk``` 

ANDROID_SDK_ROOT
```C:\Users\${user}\AppData\Local\Android\Sdk```

JAVA_HOME
```C:\Program Files\Java\jdk1.8.0_271```

JRE_HOME
```C:\Program Files\Java\jre1.8.0_271\jdk1.8.0_271``` ou ```C:\Program Files\Java\jre1.8.0_271\jdk1.8.0_271\bin```

PATH
```C:\Users\${user}\AppData\Local\Android\sdk\platform-tools```

PATH
```C:\Users\${user}\AppData\Local\Android\sdk\tools\bin```

PATH
```C:\Users${user}\AppData\Local\Android\sdk\emulator```

PATH
```C:\Users\${user}\AppData\Local\Android\sdk\build-tools${version}```

PATH
```C:\Program Files\java${jdkVersion}\bin```

(Si il vous dis que java n'est pas a la bonne version dans Path remonter en premiere position  ```C:\Program Files\Java\jdk1.8.0_271\bin``` )



# autorisé l'ajax dans votre application 
## (meme en http)
 

## dans Config.xml 
 
  - remplacer le widget par :
 ```
 <widget id="com.yourapp" version="1.0.0" xmlns="http://www.w3.org/ns/widgets" xmlns:gap="http://phonegap.com/ns/1.0" xmlns:android="http://schemas.android.com/apk/res/android" xmlns:cdv="http://cordova.apache.org/ns/1.0">

```

 - remplacer le contenu de android par :
 
```
    <platform name="android">
        <edit-config file="app/src/main/AndroidManifest.xml" mode="merge" target="/manifest/application">
            <application android:usesCleartextTraffic="true" />
        </edit-config>
    </platform>'
```

#  Erreur rencontrer

- No Java files found which extend CordovaActivity. when use “cordova build” ```solution remote la plateform et la rebuild```


- application not installed sur mobile ```car il y a une autre application avec le meme nom ou meme id```

# ajax request GET POST PUT DELETE

```
 $( document).ready(function() {
        var contenu = ''
        var total = 0
     $.ajax({
        url : 'http://127.0.0.1:8000/compte',
        type : 'GET',
        dataType : 'json',
        success : function(data){ // success est toujours en place, bien sûr !
            console.log(data)
            data.forEach(element => {
                total = total + Number(element.sommes);
                contenu += `
                <tr>
                   
                    <td id="intitule${element.id}">${element.intitule}</td>
                    <td><span id="sommes${element.id}">${element.sommes}</span> €</td>
                    <td id="date${element.id}">${element.date}</td>
                    <td id="id${element.id}">${element.id}</td>
                    <td><span class="dtr-title"></span> <span class="dtr-data"><a class="dropdown-toggle addon-btn" data-toggle="dropdown" aria-expanded="true">
                        <i class="icofont icofont-ui-settings"></i>
                    </a>
                    <div class="dropdown-menu dropdown-menu-right">
                        <a class="dropdown-item" href="#" data-toggle="modal" data-target="#modifier" onclick="modifier(${element.id})"><i class="icofont icofont-ui-edit" onclick="modifier(${element.id})"></i>Modifier</a>
                        <div role="separator" class="dropdown-divider"></div>
                        <a class="dropdown-item" href="#" onclick="supprimer(${element.id})"><i class="icofont icofont-ui-delete"></i>Supprimer</a>
                        
                       
                    </div></span></td>
                </tr>
                       `
                      
               $('#tablecompte').html(contenu)
               $('#total').html(total)
               $('#titrecompte').html(total)
            });
        },
 
        error : function(resultat, statut, erreur){
 
        }
 
     });
    });

    function modifier (id){

        var id = $('#id'+id).html()
        var intitule = $('#intitule'+id).html()
        var sommes = $('#sommes'+id).html()
        var date = $('#date'+id).html()
        var url = 'http://127.0.0.1:8000/compte/'+ id

        $('#modintitule').val(intitule)
        $('#modsommes').val(sommes)
        $('#moddate').val(date)
        $('#modid').val(id)

    }

    function supprimer (id){
        
        $.ajax({
            url: 'http://127.0.0.1:8000/compte/'+ id, 
            dataType: 'json',
            contentType: 'application/json',
            headers : {
                'Content-Type' : 'application/x-www-form-urlencoded; charset=UTF-8'
            },
            type: 'DELETE', 
            success : function(data){ // success est toujours en place, bien sûr !
             document.location.reload()
               
            },
            error : function(resultat, statut, erreur){
                document.location.reload()
            }
        })




    }

    $("#updatebutton").on("click", function() {
        id = $('#modid').val()
       
        $.ajax({
            url: 'http://127.0.0.1:8000/compte/'+ id, 
            dataType: 'json',
            contentType: 'application/json',
            headers : {
                'Content-Type' : 'application/x-www-form-urlencoded; charset=UTF-8'
            },
            type: 'PUT', 
            data: $('#update').serialize(), 
            success : function(data){ // success est toujours en place, bien sûr !
                console.log(data)
               document.location.reload()
            },
            error : function(resultat, statut, erreur){
                console.log(resultat)
                document.location.reload()
            }
        })
});


    $("#addbutton").on("click", function() {
        
        $.ajax({
            url: 'http://127.0.0.1:8000/compte', 
            dataType: 'json',
            contentType: 'application/json',
            headers : {
                'Content-Type' : 'application/x-www-form-urlencoded; charset=UTF-8'
            },
            type: 'POST', 
            data: {myData : $('#add').serialize()}, 
            success : function(data){ // success est toujours en place, bien sûr !
                console.log(data)
               document.location.reload()
            },
            error : function(resultat, statut, erreur){
                console.log(resultat)
                document.location.reload()
            }
        })
});
```
# add logo
- après avoir build crée un dossier dans  ```www/res/icon```
- ajouter le code suivant dans  ```config.xml -> dans <platform name="android">`` 
```

<icon src="www/res/icon/logo.png"  />
<icon src="www/res/icon/logo.png"  />
            
 
```
