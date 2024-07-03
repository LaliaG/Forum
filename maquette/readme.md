On a 6 dépendances à dire leur utilité MySQL : JPA et driver MySQL et on génère notre application
Au début il faut configurer. Depuis Intellij on va se créer une Base De Données MySQL. On donne un nom à cette BDD. Une configuration basique d'une BDD. Il faut un nom l'utilisateur et un mot de passe car on va s'en reservir pour la config. Le port 3306 il va falloir le retenir car on va s'en servir pour la configuration. Si on a pas encore les drivers faudra les télécharger
Test de connexion: 
DBMS: MySQL (ver. 8.0.35)
Case sensitivity: plain=lower, delimited=lower
Driver: MySQL Connector/J (ver. mysql-connector-j-8.2.0 (Revision: 06a1f724497fd81c6a659131fda822c9e5085b6c), JDBC4.2)

Ping: 53 ms
SSL: yes. Cliquer sur appliquer et ok pour valideron voit que notre BDD est bien créée et qu'il n' a rien à l'intérieur pour l'instant. Il faut créer le Schéma.(?) On peut voir l'utilisateur root qui est là. Pour la configuration on va dans notre partie ressources dans application properties: on va mettre toutes informations pour se connectet à notre BDD:
- premier élément url à notre BDD spring.datasource.url et là on va aller chercher l'url de notre BDD pour la retrouver on va sur notre BDD clique droit properties on copie colle jdbc:mysql://localhost:3306 on ajoute /forum pour accéder à notre BDD. On va rajouter deux champs pour mettre notre utilisateur et notre mot de passe saisis toute à l'heure. Et un dernier champ si on veut mettre automatiquement à jour le schéma de la BDD à chaque fois qu'on lance l'application on va remettre spring.jpa.hibernate.ddl-auto=update et va le mettre en mode update
spring.datasource.url=jdbc:mysql://localhost:3306
spring.datasource.username=root
spring.datasource.password=Laliayou19
spring.jpa.hibernate.ddl-auto=update
Voila normalement on a bien configuré notre application