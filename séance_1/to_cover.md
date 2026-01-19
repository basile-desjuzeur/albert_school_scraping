# W1 - 1

- partiel, présentation ...
  
- motivation : pourquoi pandas & web scraping c'est utile ?

	- scraping utilisé partout :
    	- veille de prix de concurrents : ex:n8n
    	- travail de tous les jours, stucturer des infos issues du web : ex : evalmee
    	- llm : créer des datasets
	>> récupérer de la donnée sur internet

	- pandas : bibliiothéque de base pour manipuler des données tabulaires : les sauvegarder dans des fihciers, aggr&éger, cleaner, inspecter ...
	>> traiter cette donnée

- organisation : 8 x 3 heures de cours (4 semaines), théorique et pratique
  - un QCM : 30 min 20%
  - un midterm : 60 min 30%
  - un final : 60 min 50%

## 1. Comment marche internet ? HTTP 101

- internet basics : un réseau d'ordinateur connecté, qui ont des adresses 
  ping www.wikipedia.org
  ping adresse ip
  test depuis browser

- comment marche http / https (hypertext transfert protocol) >> ce sont des requêtes entre différents appareils connectés pour se partager du texte

url (uniform ressource locator) : https://fr.wikipedia.org/wiki/Albert_School

  - avec le protocole https
  - va sur le serveur de wikipedia
  - dans les wiki (dossier)
  - donne moi la page de albert school
  
curl https://fr.wikipedia.org/wiki/Albert_School 

curl https://fr.wikipedia.org/wiki/Albert_School >> test.html

firefox test.html

>> pas mis en page on verra pk

- les status de réponse de ces requêtes (63 en tout ...)
	- 2** : success , 200 OK
	- 4** : erreur 
	[source](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)
		- 400 : bad request >> mal formulée
		- 403 : requête non permise
		- 404 : serveur not found (légende)

Comment on fait tout ça en python ?

>> notebook pt1

>> exercice rapide

## 2. Qu'est ce qu'une page web ? Comment elle est structurée ? HTML 101

- html structure
  - head
  - body

à partir de l'exemple simple template.html

- les tags (p, h1, ..., h6, ul, ol, li, href)
- l'intérêt de css, décommenter la ligne css de template.html

## 3. BeautifoulSoup pour parser du HTML

- 

## 4. En pratique comment faire ?

- trouver ce qu'on cherche
- inspecter la page (démo browser avec l'outil dévelopeur)
  - time permitting, démo de la console
    - console.log("Hello world")
    - window.scrollTo({ top: document.body.scrollHeight, behavior: "smooth" });
    - document.body.style.background = "#111";
    - document.body.style.color = "#fff";

- requêter le site avec requests
- parser avec bs4
- mettre tout ca dans une dataframe

## 5. TP notebook