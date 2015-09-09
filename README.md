# smooths croll (défilement fluide) 
## en jQuery (et sans plugin ^^)

Vous savez faire des sites "one page" avec des ancres (pour naviguer rapidement) ?␣␣
Donnez à vos page un côté plus "esthtique" grace au Smooth Scroll.␣␣
_Ce tutoriel demande des connaissances en jQuery et html_

## Éatpe 1
Inclure la bibliothèque jQuery dans votre Head
'<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>'

## Étape 2
Faites vos ancres (ou si vous avez un trou de mémoire : )

## Étape 3
copiez-collez ce code juste avant votrebalise </body>.
Ou .nomDeVosClasse correspond au nom des classes que vous avez donnez à vos liens

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


