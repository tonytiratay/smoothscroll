# smooths croll (défilement fluide) 
## en jQuery (et sans plugin ^^)

Vous savez faire des sites "one page" avec des ancres (pour naviguer rapidement) ?
Donnez à vos page un côté plus "esthtique" grace au Smooth Scroll.
_Ce tutoriel demande des connaissances en jQuery et html_

## Éatpe 1
Inclure la bibliothèque jQuery dans votre Head
```html
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
```

## Étape 2
Faites vos ancres (ou si vous avez un trou de mémoire : [ce site est génial](https://openclassrooms.com/courses/apprenez-a-creer-votre-site-web-avec-html5-et-css3/creer-des-liens) )

## Étape 3
copiez-collez ce code juste avant votrebalise </body>.
Ou .nomDeVosClasse correspond au nom des classes que vous avez donnez à vos liens
```html
<script>
	$(document).ready(function() {
		$('.nomDeVosClasse').click( function() { // Au clic sur un élément
			var page = $(this).attr('href'); // Page cible
			var speed = 750; // Durée de l'animation (en ms)
			$('html, body').animate( { scrollTop: $(page).offset().top }, speed ); // Go
			return false;
		});
	});
</script>
```

Ce qui vous donne (pour un site TRÈÈÈÈÈSSSSSS basique) : 
```html
<DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="utf-8">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
  </head>
  <body>

    <ul class="menu">
	      <li><a class="nomDeVosClasse" href="#page-1">Page1</a></li>
	      <li><a class="nomDeVosClasse" href="#page-2">Page 2</a></li>
    </ul>

    <div id="page-1">
      <h2>Page 1</h2>
      <img src="http://placekitten.com/g/200/300"/>
      <img src="http://placekitten.com/g/400/300"/>
      <img src="http://placekitten.com/g/500/300"/>
      <img src="http://placekitten.com/g/400/400"/>
      <img src="http://placekitten.com/g/200/300"/>
      <img src="http://placekitten.com/g/400/300"/>
      <img src="http://placekitten.com/g/500/300"/>
      <img src="http://placekitten.com/g/400/400"/>
    </div>

    <div id="page-2">
      <h2>Page 2</h2>

      <img src="http://placekitten.com/g/200/300"/>
      <img src="http://placekitten.com/g/400/300"/>
      <img src="http://placekitten.com/g/500/300"/>
      <img src="http://placekitten.com/g/400/400"/>
      <img src="http://placekitten.com/g/200/300"/>
      <img src="http://placekitten.com/g/400/300"/>
      <img src="http://placekitten.com/g/500/300"/>
      <img src="http://placekitten.com/g/400/400"/>
    </div><!-- /page-2 -->

  <script>
  	$(document).ready(function() {
  		$('.nomDeVosClasse').click( function() { // Au clic sur un élément
  			var page = $(this).attr('href'); // Page cible
  			var speed = 750; // Durée de l'animation (en ms)
  			$('html, body').animate( { scrollTop: $(page).offset().top }, speed ); // Go
  			return false;
  		});
  	});
  </script>
  </body>
</html>
```
