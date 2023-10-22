# IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-
Ce projet est une application Java de gestion de données de machines et de salles, en utilisant Hibernate pour la persistance des données, RMI pour la communication à distance et JNDI pour la localisation des services requis.

Le projet est une application Java de gestion de données de machines et de salles. Il utilise le framework Hibernate pour la persistance des données, ce qui permet de stocker les informations dans une base de données de manière efficace. Pour la communication à distance entre les différentes parties de l'application, le projet fait usage du protocole RMI (Remote Method Invocation). De plus, il utilise l'API JNDI (Java Naming and Directory Interface) pour la localisation des services nécessaires. L'application facilite des opérations courantes telles que la création, la mise à jour, la suppression et la récupération des informations relatives aux machines et aux salles. L'architecture du projet semble être conçue pour permettre une utilisation distribuée et efficace de la gestion des données.

# Expliquation :
- On cherche à accéder à deux types d'entités distantes, à savoir Machine et Salle, en utilisant respectivement les interfaces IDao<Machine> et IDao<Salle>, afin de se connecter à ces entités distantes via RMI en utilisant leurs URL.
- L'interface IDao<T> étend l'interface Remote pour permettre aux méthodes définies d'être invoquées à distance. Les méthodes déclarées comprennent les opérations courantes de création, mise à jour et suppression, ainsi que des opérations de recherche de données.
- La classe Machine qui est sérialisable possède des champs privés tels que id, ref, marque, prix et salle avec des méthodes d'accès correspondantes. Elle possède également des constructeurs pour initialiser ces champs lors de la création d'instances de la classe. De plus, il existe des méthodes d'accès pour obtenir et modifier ces champs.
La méthode toString() est également implémentée pour fournir une représentation sous forme de chaîne de caractères des informations de la machine, notamment son ID, sa référence, sa marque et son prix.
De plus, il y a une méthode spécifique findMachinesBySalle(Salle s) qui permet de récupérer toutes les machines associées à une salle donnée.
- La classe Salle, également sérialisable, qui possède des champs privés tels que id et code, avec des méthodes d'accès pour accéder et modifier ces champs, ayant des constructeurs qui permettent d'initialiser ces champs lors de la création d'instances de la classe. La classe comporte également une méthode toString() qui retourne la représentation sous forme de chaîne de caractères du code de la salle.
# Démonstration:
### Gestion des salles :
#### Ajout d'une salle 

![ajout salle](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/e02699a9-2cd0-44a1-bcc8-2e83f5f0705a)

![ajout avec succes](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/924130c2-1ebb-44d2-8074-93bd4d3dbd4d)

La salle est ajoutée avec succes !

#### Modification d'une salle

![modif salle](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/334e0e74-efba-4230-9e1f-261afc9b4ec8)

![modif sallepar succes](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/072accfc-bbae-4e56-bf80-f7251da53eb6)

La salle est modifiée avec succes !

#### Suppréssion d'une salle

![supp salle](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/4247acd8-b992-403e-abfc-b55fc9612ca1)

![supp salle avec succes](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/aa8c9ab5-8681-4bbc-a8ea-29e3d6315c9e)

La salle est supprimée avec succes !

### Gestion des machines :

#### Ajout d'une machine 
![AJOUT MACHINE SALLE AVEC SUCCES](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/f2be58b2-0c21-4836-a4f6-a073dd92b8f8)

![AJOUT MACHINE SALLE](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/1be25893-6138-42f6-b2e5-4c11141c694a)

La machine d'une salle est ajoutée avec succes !

#### Modification d'une machine
![MODIF MACHINE SALLE REF](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/68b97f1c-2d89-43e4-8570-56874f9dcd39)

![MODIF mach SALLE REF AVEC SUCCES](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/9707b6fd-176d-4fe5-88b1-021fa208fd3f)

La machine d'une salle est modifiée avec succes !
#### Suppréssion d'une machine
![supp machine salle](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/059dc278-ff19-4c96-9d0d-573939097600)

![suupp salle machine avec succes](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/59a56e4a-bafc-4b7b-acc7-da173e4b2003)

![SUPP MACHINE SALLE AVEC SUCCES](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/3a3a3221-0b87-4d7d-9809-cd0606da7fee)

### Affichage des machines par salle :
![afficher les machines d'une salle](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/eaa5aa16-6f4e-4ce6-a75d-6c0ca394929f)

# Base de données :
![dbmachine](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/f5d887ba-0668-4655-864a-1ef2eeab83a5)

# Diagramme de classe du projet :
![conception salle machine](https://github.com/IkramKhardali/IkramKhardali-Gestion-Salle-Machine-en-RMI-JNDI-/assets/127056219/3cea6c9e-fb98-452c-becf-67b4a2304c29)





