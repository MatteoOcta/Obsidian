### Changer un lien 

```js
const videoConst = document.querySelector(".jg_row1 .jg_subcatelem_txt__link[title='Video']"); //Selecteur CSS

if(videoConst){ //On vient vérifier que la const a bien récupere une balise
	videoConst.setAttribute("href", "/test") //Changement d'attribut
}
```

### Menu burger en menu principal 

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