# Architecture globale de l'application 
## MVC (Modèle Vue Contrôleur) en utilisant:
 
   Coté métier (Dans le langage Java):

	Un convertisseur opensource dénommé "docs-to-pdf-converter-1.8", développé par Yeo Kheng Meng.
       
	Des processus de gestion des connexions utilisateurs, des conversion et des hébergements des fichiers				
							
   Controlleur (Sous forme de servlets)					
					
   Coté Vue (Des pages jsp formattées pour faciliter la connexion et l'échanges des fichiers)

## L'architecture de la couche donnée 
  La persistance des données (objets relationnels) des utlisateurs sera géré par le framework Hibernate.
  
  Les données seront ensuite stockés dans des BDD MySQL.

## la manière de gestion de demandes des clients 
 Un service client de qualité permet également de fidéliser les clients, en facilitant la gestion et le traitement.
 
## les technologies choisires 
 github pour placer l'application et d'une autre part faire le colaboration et notifier l'avancement dans la réalisation de projet.
	
 framwork Spring pour construire et définir l'infrastructure d'une application java.
	
 plateforme Cloud Openshift pour le déploiement de l'application.
 

# Fonctionnement général
## Connexion du Client:
Le client doit se connecter en utilisant son e-mail et son password s'il possède déjà un compte. Dans le cas échéant, il va devoir créer un nouveau compte.

<p align="center">
  <img src=![image](https://user-images.githubusercontent.com/44125253/49077765-69b18000-f23c-11e8-8f66-b74872cd7b25.png)>
</p>

<center> ![image](https://user-images.githubusercontent.com/44125253/49077765-69b18000-f23c-11e8-8f66-b74872cd7b25.png)</center>
