# Architecture globale de l'application 
## MVC (Modèle Vue Contrôleur) en utilisant:
 
   Coté métier (Dans le langage Java):

	Un convertisseur opensource dénommé "docs-to-pdf-converter-1.8", développé par Yeo Kheng Meng.
       
	Des processus de gestion des connexions utilisateurs, des conversion et des hébergements des fichiers.			
							
   Controlleur (Sous forme de servlets)					
					
   Coté Vue (Des pages jsp formattées pour faciliter la connexion et l'échanges des fichiers)

## L'architecture de la couche donnée 
  La persistance des données (objets relationnels) des utlisateurs sera géré par le framework Hibernate.
  
  Les données seront ensuite stockés dans des BDD MySQL.
  
![image](https://user-images.githubusercontent.com/44125253/50881625-81a32480-13e2-11e9-8ee0-bd7432c83553.png)


## la manière de gestion de demandes des clients 
 Un service client de qualité permet également de fidéliser les clients, en facilitant la gestion et le traitement.
Plusieurs entités du convertisseur seront déployés sous forme de Thread-Pool. 

![alt text](https://upload.wikimedia.org/wikipedia/commons/0/0c/Thread_pool.svg)
 
 Ces derniers receveront les demandes de conversions des clients dispatchés par le controleur MVC (la servlet J2E), qui sont à leurs tour stockés dans une file d'attente triée par date d'arrivée (indépedemment du client qui a lancé la requête).
 
## les technologies choisires 
 github pour placer l'application et d'une autre part faire le colaboration et notifier l'avancement dans la réalisation de projet.
	
 framwork Spring pour construire et définir l'infrastructure d'une application java.
	
 plateforme Cloud Openshift pour le déploiement de l'application.
 

# Fonctionnement général
## Connexion du Client:
Le client doit se connecter en utilisant son e-mail et son password s'il possède déjà un compte. Dans le cas échéant, il va devoir créer un nouveau compte.

![image](https://user-images.githubusercontent.com/44125253/49077765-69b18000-f23c-11e8-8f66-b74872cd7b25.png)

## Upload du fichier:
L'utilisateur sera alors mené vers une page web ou il pourra uploader un fichier dans l'un des formats: Docx ou Pptx. Il pourra aussi choisir s'il veut ou non recevoir le fichier converti par e-mail.

![image](https://user-images.githubusercontent.com/44125253/49079419-cfa00680-f240-11e8-8967-6ed8d23b39ab.png)

Une fois l'opération validée, il sera redirigé vers une autre page montrant le statut chaque conversion qu'il a lancé (En attente, en cours, terminée). Lorsqu'un document est converti, le client disposera de 5 minutes pour le télécharger depuis la page de statut. Le fichier sera supprimé si le délai est dépassé. 

Un utilisateur ne peut effectuer que 2 conversions à la fois.
