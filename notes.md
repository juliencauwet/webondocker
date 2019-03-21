#DOCKER
Le Dockerfile doit être à la source du projet
dockerfile-maven-plugin permet de générer directement l'image Docker du projet.
Il faut créer le repo sur DockerHub
Il faut spécifier la destination (URL) du déploiement de l'application dans le secteur <distributionManagement> de Maven:

ex:
<distributionManagement>
    <repository>
      <uniqueVersion>false</uniqueVersion>
      <id>corp1</id>
      <name>Corporate Repository</name>
      <url>scp://repo/maven2</url>
      <layout>default</layout>
    </repository>
    ...
</distributionManagement>
