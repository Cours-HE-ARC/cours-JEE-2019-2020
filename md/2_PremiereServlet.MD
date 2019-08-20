# Première Servlet

Ce tutoriel à pour but de développer une servlet Java via l'IDE Spring Tools

## Sommaire

1. [Configuration d'un serveur d'application](#configuration-dun-serveur-dapplication)
2. [Configuration de l'application Web](#configuration-de-lapplication-web)
3. [Création d'une servlet](creation-dune-servlet)


### Configuration d'un serveur d'application

Afin de pouvoir exécuter une servlet Java, il est nécessaire de configurer un container applicatif (serveur d'application JEE). Nous allons utiliser Apache Tomcat précédemment installé. 

- Dans l'IDE Spring Tools allez dans _**File -> New -> Other...**_ 

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/set-tomcat-1.png)

- Choisir **_Server_**  (utiliser la barre de recherche en haut) 

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/set-tomcat-2.png)

- **_Next_**

- Choisir _**Tomcat v9.0 Server**_  

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/set-tomcat-3.png) 

- **_Next_**

- Spécifier le chemin d'installation de Apache Tomcat (répertoire ou il à été dézipper), ainsi que la version de Java à utiliser (celle précédemment configurer):

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/set-tomcat-4.png)

- **_Finish_** 

### Configuration de l'application Web

- **_File -> New -> Dynamic Web Project_**

- Donner un nom au projet, spécifier l'environnement d'exécution (le serveur Apache Tomcat précedemment configuré):

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/premiere-servelt-app-1.png) 

- **_Finish_**

Si tout s'est bien passé, le panneau **_Project Explorer_** doit correspondre à celà:  

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/premiere-servelt-app-2.png)

#### Ajout de l'application au serveur et démarrage 

- Clic Droit sur la zone serveur dans le volet du bas: 

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/add-app-to-server.png)

- Ajouter l'application (zone _Available_) dans la zone _Configured_:

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/add-app-to-server-2.png)

- _**Finish**_

#### Test de l'application

- Clic droit sur le projet de l'application, **_Run as -> Run on Server_**:

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/app-run.png)

Celà aura pour effet de démarrer le serveur ainsi que l'application qu'il contient, vous devriez voir ceci dans les logs du serveurs :

> août 12, 2019 4:56:53 PM org.apache.coyote.AbstractProtocol start
> INFOS: Démarrage du gestionnaire de protocole ["http-nio-8080"]
> août 12, 2019 4:56:53 PM org.apache.coyote.AbstractProtocol start
> INFOS: Démarrage du gestionnaire de protocole ["ajp-nio-8009"]
> août 12, 2019 4:56:53 PM org.apache.catalina.startup.Catalina start
> INFOS: Le démarrage du serveur a pris [1 019] millisecondes

En état l'application ne répond à aucun requête, aucun point d'entrée http n'est défini.

### Création d'une servlet

- Clic droit sur le projet
- **_New -> Servlet_**
- Remplissez les champs **_Java package, et Class name_**:

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/hello-servlet.png)

- _**Finish**_

- Redémarrer le serveur, et tester l'url http://localhost:8080/PremiereServlet/HelloServlet

### Exercices
#### Exercice 1 

- Modifier la servlet afin qu'elle affiche **_"Hello "_** suivi de votre prénom
  - Utilisation de paramètres de requêtes
  
#### Exercice 2

- Modifier la servlet, afin qu'elle réponde au path _**/hello**_ (à la place de _HelloServlet_)

#### Exercice 3

- Créer une nouvellet servlet, afin qu'elle affiche **_"Hello "_** suivi de votre prénom
  - Utilisation de paramètres de path (style REST)




