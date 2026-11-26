# ED-mécanique

Site vitrine d'un garage : **mécanique générale et carrosserie**. Prix fait sur place, après inspection.
Sur rendez-vous ou premier arrivé, premier servi.

Site statique, sans dépendance à installer : `index.html`, une feuille de style et un petit script.

```
index.html              la page (une seule page, avec des sections)
assets/css/style.css    le style : rouge, noir et blanc, typographie Barlow
assets/js/site.js       menu mobile, en-tête au défilement, formulaire qui prépare un texto
assets/img/             logo (favicon.svg) et photos
```

## Voir le site sur son poste

```powershell
python -m http.server 5120 --directory .
```

Puis ouvrir http://localhost:5120.

## Le formulaire de rendez-vous

Aucun serveur et aucune donnée stockée. Sur téléphone, le bouton « Envoyer ma demande par texto » ouvre l'appli
Messages du client avec la demande déjà écrite (nom, téléphone, véhicule, service, date, remarques) : le client touche
Envoyer, et la demande arrive dans les textos du garage, avec le numéro du client pour lui répondre. Sur ordinateur,
le client copie le message. Pour des demandes qui arrivent toutes seules, sans ce dernier geste du client, il faudrait
un service d'envoi de textos payant (ex. Twilio) ou un formulaire reçu par courriel.

## Coordonnées affichées

Le téléphone est le vrai : **438 764-7365** (appels et textos du formulaire). Pour le changer : `index.html`
(rechercher `764-7365` et `4387647365`) et `assets/js/site.js` (`TELEPHONE` et les deux messages).

Paiement : **comptant seulement** (confirmé par le mécanicien) ; il apparaît dans les coordonnées, la FAQ, l'étape 5,
le pied de page et `paymentAccepted`.

Heures : **de 8 h à 18 h** (données par le mécanicien ; les jours ne sont pas encore précisés, donc le site n'en
affiche pas et les données pour Google n'ont pas d'`openingHours`).

Adresse : **10570, avenue Éthier, Montréal** (confirmée, avec un lien « Itinéraire » vers Google Maps ; aussi dans
l'en-tête de l'accueil, le pied de page et `address` des données pour Google).

## Mise en ligne

Adresse du site : **https://ed-mecanique.github.io/** (GitHub Pages ; dépôt `ed-mecanique/ed-mecanique.github.io`,
qui est ce dossier). Pour publier une nouvelle version : commit puis push sur `main`, le site se met à jour en moins
d'une minute. Le site est ouvert aux moteurs de recherche (adresse `canonical` vers cette adresse).

L'ancienne adresse, https://vitalemecelestin.github.io/site-mecanicien/, redirige vers la nouvelle ; l'ancien site de
démonstration est gardé dans le dossier `ancien-site/` de ce dépôt-là.

## Photos

Photos libres de droits (licence Unsplash : usage gratuit, y compris commercial, sans obligation de citer
l'auteur ; les auteurs sont tout de même cités dans le pied de page) :

| Section | Auteur | Page Unsplash |
|---|---|---|
| Accueil | Zanelle Lofty-Eaton | https://unsplash.com/photos/Ffq4-mWzhmE |
| Mécanique générale | Christian Buehner | https://unsplash.com/photos/Fd6osyVbtG4 |
| Carrosserie | Zoshua Colah | https://unsplash.com/photos/CNciVh_m1rU |
| Carrosserie (encart) | Clark Van Der Beken | https://unsplash.com/photos/CSkriQWeTVs |
| Bandeau « Le prix se fait sur place » | Tahamie Farooqui | https://unsplash.com/photos/K5624F8cipE |

Aucune de ces photos ne montre le visage d'une personne : elles illustrent le métier sans laisser croire
qu'il s'agit du mécanicien. Le mieux reste de les remplacer par de vraies photos de l'atelier et des travaux.
