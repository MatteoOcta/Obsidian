### Changer un lien 

```js
const videoConst = document.querySelector(".jg_row1 .jg_subcatelem_txt__link[title='Video']"); //Selecteur CSS

if(videoConst){ //On vient vérifier que la const a bien récupere une balise
	videoConst.setAttribute("href", "/test") //Changement d'attribut
}
```

### Menu burger en menu principal 

Exemple : https://www.empiremariage.com/ 

```js

function toggleMenu(menu, backdrop){ //On ajoute la classe visible si elle n'est pas mise et inversement. 
 menu.classList.toggle("visible")
 backdrop.classList.toggle("visible");
}
window.addEventListener("DOMContentLoaded", (event) => { //On attend que la page est recu toutes les balises et la structure html 
	const btnConst = document.querySelector('#t3-mainnav .t3-megamenu .burger');
	const backDropConst = document.querySelector('.menu-backdrop');
	const menuConst = document.querySelector('#t3-footer .menu');
	const menuResponsiveConst = document.querySelector('.navbar-toggle');

	if(!btnConst || !menuConst){ // On vérifie si les querySelector on bien recuperer les balises 
		throw new Error("btnCost ou menuConst n'existe pas")
	}
	btnConst.addEventListener("click", function(){
		toggleMenu(menuConst , backDropConst);
	});
	backDropConst.addEventListener("click", function(){
		toggleMenu(menuConst , backDropConst);
	});
	menuResponsiveConst.addEventListener("click", function(){
		toggleMenu(menuConst , backDropConst);
	});
});

```

### Récupérer une partie d'une chaine de caractère 

Il est important de savoir qu'une chaine de caractère type string est enfaite un tableau de caractère 

On peux donc récupérer  juste une lettre en prenant sa position 
```js 
a[n - 1];
```

Mais on peux aussi récupérer toute une partie 
```js
const str = 'The quick brown fox jumps over the lazy dog.';

console.log(str.slice(31));
// Expected output: "the lazy dog."

console.log(str.slice(4, 91));
// Expected output: "quick brown fox"
```

Il est possible de récupérer l'emplacement d'une chaine de caractère 
```js
a.indexOf('is');
// Start: myFunction("praise") | Result : 3
```
