# Installation des outils
## Sommaire
1. [Java](#Java)
2. [Apache Tomcat](#apachetomcat)
3. [Spring Tools 4](#spring-tools-4)
4. [Docker](#docker)
5. [Postman](#postman)

Définir un répertoire qui contiendra les outils que nous allons installer.

### Java  

La version **Oracle de Java** est désormais payante, hormis pour une utilisation strictement privée. Dans un cadre académique nous devrons utiliser une version gratuite.  
  
Conformément à la politique de la HE-ARC, nous allons utiliser une version gratuite de Java, à savoir l'implémentation ***AdoptOpenJDK***.  
  
Java nécessite de configurer 2 variables d'environnement sur le système : ***JAVA_HOME*** et ***Path***. Il y a possibilité d'installer plusieurs versions en parallèle, mais seule la version correctement configuré par les variables d'environnements sera utilisée par le système.  
  
Via l'IDE, il sera possible de spécifier une autre version sans changer la variable d'environnement.  
#### Installation via l'installateur  
Ce mode d'installation va s'occuper de toute l'installation, y compris redéfinir la variable ***JAVA_HOME***, ce qui aura un impact sur le système dans son ensemble.  

- Télécharger  **AdoptOpenJdk**, ici : [https://adoptopenjdk.net/release.html](https://adoptopenjdk.net/releases.html) 

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/adopt-version-choix.png)  

- Choisir l'installation **installateur** (ou tar.gz) ***en bleu***

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/adopt-version-format-choix.png)  
  

#### Instation manuelle (via archive zip)  
  
- Télécharger  **AdoptOpenJdk**, ici : [https://adoptopenjdk.net/release.html](https://adoptopenjdk.net/releases.html)  

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/adopt-version-choix.png)  
- Choisir l'installation zip (ou tar.gz) ***en gris*** et non pas la version installateur

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/adopt-version-format-choix.png)  

- Dezipper le répertoire

##### Optionnel, configuration de Java pour le système

- Configurer la variable ***JAVA_HOME***, ici: [https://docs.oracle.com/cd/E19509-01/820-3208/inst_cli_jdk_javahome_t/](https://docs.oracle.com/cd/E19509-01/820-3208/inst_cli_jdk_javahome_t/)

- Ajouter le répertoire **/bin** de Java à la variable d'environnement ***PATH***, ici: [https://warwick.ac.uk/fac/sci/dcs/people/research/csrcbc/teaching/howto/javapath/](https://warwick.ac.uk/fac/sci/dcs/people/research/csrcbc/teaching/howto/javapath/)

##### Test de l'instalation

- Ouvrir une interface cli (terminal, console)
- Lancer la commande `java -version`
- La réponse obtenu doit ressembler à celle ci

> openjdk version "11.0.4" 2019-07-16 <br>
> OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.4+11) <br>
> OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.4+11, mixed mode)


### Apache&nbsp;Tomcat  

Apache Tomcat(c) est un container de servlet fournissant les fonctionnalités de bases pour développer des application Java EE. Ce n'est pas un container standardise JEE, mais il conviendra pour le cours.   
  
- Télécharger Apache Tomcat, ici : [https://tomcat.apache.org/download-90.cgi](https://tomcat.apache.org/download-90.cgi)  
- Choisir la version adapté à votre OS sous la zone Core  
![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/tomcat9-core.png)  
- Dezipper l'archive
  
### Spring Tools 4  

Spring Tools est un IDE basé sur Eclipse et fourni par Pivotal(c), qui maintient le framework Spring. Il fourni le nécessaire pour tout développement basé sur Java EE et Spring.   
- Télécharger Spring Tools ici: [https://spring.io/tools](https://spring.io/tools)  
- Dezipper l'archive  
- Démarrer l'IDE 
- Spécifier un répertoire pour le workspace (un seul sera utilisé pour le cours) 
- Aller dans **_Window -> Preferences_**
- Cliquer sur **_Add..._**
- Choisir _**Standard VM**_ puis **_Next_**
- Définir le chemin d'installation de Java (AdoptOpenJDK), puis _**Finish**_

![](https://github.com/Cours-HE-ARC/cours-JEE-2019-2020/blob/master/pratique/images/set-java-ide-buid-path.png)  

- Ne pas oublier de cocher la version de Java dans la liste, puis _**Apply and Choose**_
 
### Docker

L'évolution des travaux pratiques de ce cours vous nous amener à utiliser des outils supplémentaires, telles que:
- Mysql, PostgresSql ou n'imposte quelles base de données Sql
- Apache ActiveMq ou n'importe quelle bus de message standard JMS

### Postman

Postman est un client http gratuit, qui va permettre de tester les points d'entrées _http_.

- Télécharger Postman, ici : [https://www.getpostman.com/downloads/](https://www.getpostman.com/downloads/)
