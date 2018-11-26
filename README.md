On observe que la requête curl  https://fr.wikipedia.org/wiki/CURL elle permet de récupérer 
Le code HTML qui est affiche sur le terminal et on ouvrent cette page HTML dans notre navigateur elle nous affiche le même code source .
On déduit que l’utilisation du curl elle permet d’envoyer des requêtes au serveur puis elle affiche le résultat du retour du serveur.
Et en navigateur cd sont des echanges HTTP

2- l'execution de la commande : curl https://httpbin.org/image
   Le code de retour : 
{"message": "Client did not request a supported media type.", "accept": ["image/webp", "image/svg+xml", "image/jpeg", "image/png", "image/*"]}

Requete pour png  : curl -X GET -k --header 'Accept: image/png' --output 'C:\Curl\y.png'  https://httpbin.org/image
Requete pour jpeg: curl -X GET -k --header 'Accept: image/jpeg' --output 'C:\Curl\y.png'  https://httpbin.org/image

3- Requete Wikipedia :


curl -X GET --header 'Accept: application/json' 'https://en.wikipedia.org/w/api.php?action=query&format=json&prop=revisions&titles=Bertrand%20Russell&rvprop=ids%7Ctimestamp%7Ccomment%7Cuser&rvstart=2017-08-01T11%3A21%3A55.000Z&rvend=2017-07-29T11%3A21%3A55.000Z' 





Par navigateur :
https://en.wikipedia.org/w/api.php?action=query&format=json&prop=revisions&titles=Bertrand%20Russell&rvprop=ids%7Ctimestamp%7Ccomment%7Cuser&rvstart=2017-08-01T11%3A21%3A55.000Z&rvend=2017-07-29T11%3A21%3A55.000Z 